# Lucid

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
