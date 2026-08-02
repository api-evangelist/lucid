---
name: Create and share a Lucid document
description: Create a Lucid document (blank, from a standard import file, or copied from a template), then grant a collaborator access and hand back a share link.
api: openapi/lucid-rest-api-openapi.yml
operations:
  - createDocument
  - createDocumentWithStandardImport
  - copyDocument
  - putDocumentUserCollaborators
  - createDocumentShareLink
  - getOrExportDocument
generated: '2026-08-01'
method: generated
source: openapi/lucid-rest-api-openapi.yml + conventions/lucid-conventions.yml
---

# Create and share a Lucid document

Base URL `https://api.lucid.co`. Every call needs an `Authorization: Bearer <token>` header — either a
Lucid API key or an OAuth 2.0 access token (see `authentication/lucid-authentication.yml`).

## Scopes

Document creation and editing needs a `*.document.content` scope for the target product
(`lucidchart.document.content`, `lucidspark.document.content`, `lucidscale.document.content`).
Read-only flows can use the `:readonly` variants. The full list is in `scopes/lucid-scopes.yml`.

## Steps

1. **Pick a creation path.**
   - Blank document → `createDocument` (`POST /v1/documents`). Supply `title` and `product`.
   - From a Visio/Gliffy/draw.io/Mermaid/AWS file → `createDocumentWithStandardImport`
     (`POST /v1/documents/create`).
   - From an existing document as a template → `copyDocument` (`POST /v1/documents/copy`).
2. **Add a collaborator.** `putDocumentUserCollaborators`
   (`PUT /v1/documents/{id}/shares/users/{userId}`) creates or updates one user's role on the
   document. For a whole team use `putDocumentTeamCollaborator`.
3. **Or mint a share link.** `createDocumentShareLink`
   (`POST /v1/documents/{id}/shares/shareLinks`) when the recipient is not a named user.
   `updateDocumentShareLink` and `deleteDocumentShareLink` manage it afterwards.
4. **Hand back a rendering if asked.** `getOrExportDocument` (`GET /v1/documents/{id}`) returns the
   document; set the export format with the `Accept` header (PNG, PDF, JPEG, SVG, CSV). An
   unsupported value returns `415`.

## Rules

- **There is no idempotency key.** Retrying a failed `createDocument` creates a second document.
  Before retrying, call `searchDocuments` with the title and a `lastModifiedAfter` bound to check
  whether the first attempt landed.
- **`403` is the dominant failure**, not `401` — 124 of the REST spec's operations declare a `403`.
  It usually means the token's scope set does not cover the requested product, not that the token
  is invalid. Check the scope for the product you passed.
- **Acting on behalf of another user** requires the `Lucid-Request-As` header and account-owner or
  document-admin permissions.
- **Rate limit:** document search is capped at 300 requests per 5 seconds per account and returns
  `429`. No `Retry-After` header is published — back off exponentially.
