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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Lucid Software Inc. is the visual collaboration company behind the Lucid Suite — Lucidchart (intelligent diagramming), Lucidspark (virtual whiteboarding) and Lucidscale (cloud visualization) — plus the Lucid Cloud, Process and Enterprise Shield accelerators and airfocus. The Lucid Developer Platform at developer.lucid.co publishes three OpenAPI-described surfaces: the Lucid REST API on api.lucid.co for documents, folders, sharing, embeds, comments, teams, repositories, legal holds, licenses and audit logs; the Lucid Data API on data.lucid.app for the structured data sets, collections, schemas and data items that back data-linked diagrams; and a SCIM 2.0 API on users.lucid.app for enterprise user and group provisioning. Lucid also ships an in-editor Extension API (lucid-extension-sdk plus the lucid-package CLI), an Embed SDK, and an OAuth-gated remote MCP server at mcp.lucid.app that lets AI clients search, read, edit and create Lucid documents. Lucid is privately held and trades on secondary markets.

**Areas:** Visual Collaboration · Diagramming · Whiteboarding · Productivity · Software-as-a-Service · Cloud Visualization · SCIM · Identity · Data · MCP

## Lucid on APIs.io

Everything profiled for Lucid is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/lucid/](https://apis.io/providers/lucid/)** — or go straight to one of the APIs or properties below.

### APIs (37)

- [Lucid MCP Server](https://apis.io/apis/lucid/lucid-mcp-server/) — Lucid's remote Model Context Protocol server. Connects AI clients (ChatGPT, Claude, Microsoft Copilot, Cursor) to Lucid documents so they can be searched,…
- [Lucid Accounts API](https://apis.io/apis/lucid/lucid-accounts-api/) — Retrieve information about the authenticated Lucid account.
- [Lucid Audit Logs API](https://apis.io/apis/lucid/lucid-audit-logs-api/) — Retrieve audit log events that record user and admin activity across the Lucid account.
- [Lucid Cloud API](https://apis.io/apis/lucid/lucid-cloud-api/) — Manage cloud infrastructure credentials, data sources, and architecture diagrams for AWS, Azure, and Google Cloud.
- [Lucid Collection API](https://apis.io/apis/lucid/lucid-collection-api/) — Create, retrieve, update, and delete collections within a data source. A collection is a named group of data items that share a common schema (similar to a…
- [Lucid Collection Properties API](https://apis.io/apis/lucid/lucid-collection-properties-api/) — Read and update metadata properties on a collection, such as display name and configuration.
- [Lucid Create Diagram API](https://apis.io/apis/lucid/lucid-creatediagram-api/) — The CreateDiagram API from Lucid — 1 operation(s) for creatediagram.
- [Lucid Data Item API](https://apis.io/apis/lucid/lucid-data-item-api/) — Create, retrieve, update, and delete individual data items within a collection. A data item is a single record conforming to the collection's schema.
- [Lucid Data Set Grant API](https://apis.io/apis/lucid/lucid-data-set-grant-api/) — Manage access grants on data sets to control which users or applications can read or write data.
- [Lucid Data Set Properties API](https://apis.io/apis/lucid/lucid-data-set-properties-api/) — Read and update metadata properties on a data set, such as display name and configuration.
- [Lucid Data Source API](https://apis.io/apis/lucid/lucid-data-source-api/) — Create, retrieve, update, and delete data sources within a data set. A data source represents an external system whose data is synced into Lucid.
- [Lucid Document Access API](https://apis.io/apis/lucid/lucid-document-access-api/) — Create, import, copy, retrieve, update, search, export, and trash documents across the Lucid Suite, and access their contents.
- [Lucid Document Comments API](https://apis.io/apis/lucid/lucid-document-comments-api/) — Retrieve comment threads on a document, list comments within a thread, and post new comments to an existing thread.
- [Lucid Document Embedding API](https://apis.io/apis/lucid/lucid-document-embedding-api/) — Generate session tokens and render the embedded viewer iframe used to display Lucid documents in external applications.
- [Lucid Document Picker API](https://apis.io/apis/lucid/lucid-document-picker-api/) — Generate tokens and render an embedded document picker that lets users select Lucid documents from within your application.
- [Lucid Documents Collaboration API](https://apis.io/apis/lucid/lucid-documents-collaboration-api/) — Manage user and team collaborator access on individual documents, including granting, updating, and revoking collaboration roles.
- [Lucid Documents Sharing API](https://apis.io/apis/lucid/lucid-documents-sharing-api/) — Create, retrieve, update, and delete share links for documents to control external access.
- [Lucid Embedding Utils API](https://apis.io/apis/lucid/lucid-embedding-utils-api/) — Create, retrieve, delete, and change the version of embed instances on a document.
- [Lucid Folders API](https://apis.io/apis/lucid/lucid-folders-api/) — Create, retrieve, update, search, trash, and restore folders. Includes listing folder contents and root folder navigation.
- [Lucid Folders Collaboration API](https://apis.io/apis/lucid/lucid-folders-collaboration-api/) — Manage user, group, and team collaborator access on folders, including granting, updating, and revoking collaboration roles.
- [Lucid Folders Sharing API](https://apis.io/apis/lucid/lucid-folders-sharing-api/) — Create, retrieve, update, and delete share links for folders to control external access.
- [Lucid Groups API](https://apis.io/apis/lucid/lucid-groups-api/) — Endpoints that deal with org groups or teams (dependent on which bearer token is used).
- [Lucid Legal Holds API](https://apis.io/apis/lucid/lucid-legal-holds-api/) — Create and manage legal holds on a Lucid account. Legal holds prevent documents from being permanently deleted for users placed on hold.
- [Lucid Licenses API](https://apis.io/apis/lucid/lucid-licenses-api/) — View and manage product licenses assigned to users within a subscription.
- [Lucid OAuth 2.0 Tokens API](https://apis.io/apis/lucid/lucid-oauth-2-0-tokens-api/) — Create, refresh, introspect, and revoke OAuth 2.0 access tokens used to authenticate API requests on behalf of a user.
- [Lucid Rate Limits API](https://apis.io/apis/lucid/lucid-rate-limits-api/) — Retrieve current rate limit thresholds and quotas for the authenticated user.
- [Lucid Repositories API](https://apis.io/apis/lucid/lucid-repositories-api/) — Create and manage shared document repositories. Control repository membership by adding and removing users and groups.
- [Lucid Schema API](https://apis.io/apis/lucid/lucid-schema-api/) — Define and retrieve the schema for a collection, specifying the fields, types, and constraints for its data items.
- [Lucid Schemas API](https://apis.io/apis/lucid/lucid-schemas-api/) — Endpoints that deal with lucid resource schemas.
- [Lucid Service Provider Config API](https://apis.io/apis/lucid/lucid-service-provider-config-api/) — Retrieve the SCIM service provider configuration, describing supported operations, authentication schemes, and bulk/filter capabilities.
- [Lucid Sharing API](https://apis.io/apis/lucid/lucid-sharing-api/) — The Sharing API from Lucid — 1 operation(s) for sharing.
- [Lucid Subscriptions API](https://apis.io/apis/lucid/lucid-subscriptions-api/) — List and retrieve product subscriptions on the account.
- [Lucid Teams API](https://apis.io/apis/lucid/lucid-teams-api/) — Create, retrieve, update, archive, and restore teams. Manage team membership by adding and removing users.
- [Lucid Transfer Content API](https://apis.io/apis/lucid/lucid-transfer-content-api/) — Transfer ownership of a user's documents, folders, custom shape libraries, and Lucidscale objects to another user within the same account.
- [Lucid Unfurling API](https://apis.io/apis/lucid/lucid-unfurling-api/) — Retrieve metadata for Lucid document links to power rich previews, and serve direct iframe embeds for Lucid documents in external applications.
- [Lucid Users API](https://apis.io/apis/lucid/lucid-users-api/) — Retrieve, create, and search for users within the authenticated account. Includes user profile access.
- [Lucid Dataset API](https://apis.io/apis/lucid/lucid-dataset-api/) — Create, retrieve, update, and delete data sets. A data set is a top-level container that groups related data sources and their collections.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [lucid-mcp.yml](https://apis.io/servers/lucid/lucid-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Lucid Agentic Access](https://apis.io/agentic-access/lucid/lucid-agentic-access/)

#### Collections (3)

Postman and Open Collection request collections.

- [Lucid Data API](https://apis.io/collections/lucid/open-lucid-data-api/)
- [Lucid REST API](https://apis.io/collections/lucid/open-lucid-rest-api/)
- [Lucid SCIM API](https://apis.io/collections/lucid/open-lucid-scim-api/)

#### Overlays (39)

OpenAPI overlays, including conversational phrasing for each operation.

- [Lucid Accounts Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-accounts-api-phrasing-overlay/)
- [Lucid Audit Logs Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-audit-logs-api-phrasing-overlay/)
- [Lucid Cloud Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-cloud-api-phrasing-overlay/)
- [Lucid Collection Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-collection-api-phrasing-overlay/)
- [Lucid Collection Properties Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-collection-properties-api-phrasing-overlay/)
- [Lucid Creatediagram Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-creatediagram-api-phrasing-overlay/)
- [Lucid Data Api Overlay](https://apis.io/overlays/lucid/lucid-data-api-overlay/)
- [Lucid Data Item Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-data-item-api-phrasing-overlay/)
- [Lucid Data Set Grant Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-data-set-grant-api-phrasing-overlay/)
- [Lucid Data Set Properties Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-data-set-properties-api-phrasing-overlay/)
- [Lucid Data Source Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-data-source-api-phrasing-overlay/)
- [Lucid Dataset Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-dataset-api-phrasing-overlay/)
- [Lucid Document Access Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-document-access-api-phrasing-overlay/)
- [Lucid Document Comments Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-document-comments-api-phrasing-overlay/)
- [Lucid Document Embedding Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-document-embedding-api-phrasing-overlay/)
- [Lucid Document Picker Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-document-picker-api-phrasing-overlay/)
- [Lucid Documents Collaboration Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-documents-collaboration-api-phrasing-overlay/)
- [Lucid Documents Sharing Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-documents-sharing-api-phrasing-overlay/)
- [Lucid Embedding Utils Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-embedding-utils-api-phrasing-overlay/)
- [Lucid Folders Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-folders-api-phrasing-overlay/)
- [Lucid Folders Collaboration Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-folders-collaboration-api-phrasing-overlay/)
- [Lucid Folders Sharing Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-folders-sharing-api-phrasing-overlay/)
- [Lucid Groups Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-groups-api-phrasing-overlay/)
- [Lucid Legal Holds Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-legal-holds-api-phrasing-overlay/)
- [Lucid Licenses Api Phrasing Overlay](https://apis.io/overlays/lucid/lucid-licenses-api-phrasing-overlay/)
- …and 14 more published on APIs.io

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Lucid Authentication](https://apis.io/security/lucid/lucid-authentication/)
- [Lucid Domain Security](https://apis.io/security/lucid/lucid-domain-security/)
- [Lucid Trust Center](https://apis.io/security/lucid/lucid-trust-center/)
- [Lucid Vulnerability Disclosure](https://apis.io/security/lucid/lucid-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Lucid Scopes](https://apis.io/scopes/lucid/lucid-scopes/)

#### Rate limits (1)

Published request limits.

- [Lucid Rate Limits](https://apis.io/rate-limits/lucid/lucid-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://lucid.co/)
- [Documentation](https://developer.lucid.co/docs/welcome)
- [Getting started](https://developer.lucid.co/docs/welcome)
- [API reference](https://developer.lucid.co/reference/api)
- [Pricing](https://lucid.app/pricing/lucidchart)
- [Sign up](https://lucid.app/users/login?activate=lucidchart)
- [Support](https://community.lucid.co/lucid-for-developers-6)
- [Blog](https://lucid.co/solutions/engineering)
- [Security](https://lucid.co/security)
- [Compliance](https://lucid.co/security)
- [Terms of service](https://lucid.co/tos)
- [Privacy policy](https://lucid.co/privacy)
- [GitHub](https://github.com/lucidsoftware)
- [Status](https://status.lucid.co/)

## API Evangelist rating

**Kin Score 68.5** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 80.0 |
| Contract quality | 58.0 |
| Contract governance | 4.5 |
| Operational transparency | 76.3 |
| Developer ergonomics | 73.2 |
| Access clarity | 60.5 |

**Agent readiness 44.7** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | mostly (partial credit) |

**Regulatory alignment 45.1** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/lucid/](https://apis.io/providers/lucid/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Lucid: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/lucid/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
