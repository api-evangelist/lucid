# Lucid

Lucid Software Inc. — the visual collaboration company behind Lucidchart, Lucidspark and Lucidscale,
plus the Cloud, Process and Enterprise Shield accelerators and airfocus.

- Website: https://lucid.co/
- Developer portal: https://developer.lucid.co/
- Status: https://status.lucid.co/
- Trust center: https://trust.lucid.co/
- GitHub: https://github.com/lucidsoftware
- Secondary market listing: https://forgeglobal.com/lucid_stock/

## APIs

| API | Base URL | Operations | Spec |
|---|---|---|---|
| Lucid REST API | `https://api.lucid.co` | 154 | `openapi/lucid-rest-api-openapi.yml` |
| Lucid Data API | `https://data.lucid.app` | 50 | `openapi/lucid-data-api-openapi.yml` |
| Lucid SCIM API | `https://users.lucid.app/scim/v2` | 15 | `openapi/lucid-scim-api-openapi.yml` |
| Lucid MCP Server | `https://mcp.lucid.app/mcp` | OAuth-gated | `mcp/lucid-mcp.yml` |
| Lucid ChatGPT Plugin API | `https://mlai.lucid.app` | 1 | `openapi/lucid-chatgpt-plugin-openapi.yaml` |

The three OpenAPI documents were harvested operation-by-operation from Lucid's own developer
documentation MCP server (`https://lucid-developer-docs.readme.io/mcp`), which returns verbatim
OpenAPI 3.0.3 fragments out of the specs Lucid uploaded to its ReadMe hub. See the `x-harvest`
block at the top of each file.

## Known gaps

- No `/.well-known/security.txt` on any host, despite a real HackerOne bug bounty program.
- No idempotency-key contract on any of the 220 operations.
- No RFC 9457 `application/problem+json` error envelope.
- No documented rate-limit response headers (`429` is returned bare).
- No deprecation / sunset policy and no SLA.
- No AsyncAPI document and no webhook or event-subscription surface.
- No A2A agent card at `/.well-known/agent-card.json` or `/.well-known/agent.json`.
- No first-party server-side REST SDK (only the npm editor-extension toolchain).

## Note on `all/lucidchart`

`all/lucidchart/` profiles the Lucidchart product and overlaps this repo, which profiles the parent
company Lucid Software and its full developer platform. They are candidates for the duplicate
provider retirement process.
