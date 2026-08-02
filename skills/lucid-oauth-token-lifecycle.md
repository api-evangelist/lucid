---
name: Run the Lucid OAuth 2.0 token lifecycle
description: Exchange an authorization code for a Lucid access token, refresh it, introspect it to check scope and expiry, and revoke it on logout.
api: openapi/lucid-rest-api-openapi.yml
operations:
  - createOrRefreshAccessToken
  - introspectAccessToken
  - revokeAccessToken
generated: '2026-08-01'
method: generated
source: openapi/lucid-rest-api-openapi.yml + https://lucid.app/.well-known/oauth-authorization-server
---

# Run the Lucid OAuth 2.0 token lifecycle

Lucid publishes RFC 8414 authorization-server metadata at
`https://lucid.app/.well-known/oauth-authorization-server` — read it rather than hard-coding
endpoints. As probed on 2026-08-01 it advertises:

- `authorization_endpoint`: `https://lucid.app/oauth2/authorizeUser`
- `token_endpoint`: `https://api.lucid.co/oauth2/token`
- `introspection_endpoint`: `https://api.lucid.co/oauth2/token/introspect`
- `revocation_endpoint`: `https://api.lucid.co/oauth2/token/revoke`
- `grant_types_supported`: `authorization_code`, `refresh_token`
- `code_challenge_methods_supported`: `S256`, `plain`

## Steps

1. **Send the user to the browser.** Authorization must happen in a browser — a user has to
   consent. Include your `client_id`, redirect URI, the scopes you need, and a PKCE `S256`
   challenge. Add `offline_access` if you want a refresh token.
2. **Exchange the code.** `createOrRefreshAccessToken` (`POST /v1/oauth2/token`) with
   `grant_type=authorization_code`. The same operation refreshes with
   `grant_type=refresh_token`.
3. **Introspect before acting.** `introspectAccessToken` (`POST /v1/oauth2/token/introspect`)
   tells you the token's live scope set and expiry — cheaper than discovering a `403` mid-flow.
4. **Revoke on logout.** `revokeAccessToken` (`POST /v1/oauth2/token/revoke`).

## Rules

- **Scope names are product-prefixed.** `lucidchart.document.content` does not grant access to a
  Lucidspark board. Request the scope for every product your flow touches. All 143 scopes seen in
  the specs are catalogued in `scopes/lucid-scopes.yml`.
- `invalid_client` usually means an admin on the Lucid account disabled your OAuth client, not
  that the secret is wrong.
- `invalid_scopes` means the scopes are not valid **for the requested token type** — Lucid issues
  both user tokens and account tokens, and their scope sets differ.
- Unpublished apps only work for collaborators listed on the app; publish before onboarding
  external users.
- The MCP surface is a **separate** authorization server (`https://mcp.lucid.app`) with its own
  metadata and dynamic client registration. Do not reuse these tokens there.
