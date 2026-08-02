---
name: Search and export Lucid documents
description: Find documents across the Lucid Suite by keyword, owner or time window, read their structured contents, and export them in a requested format.
api: openapi/lucid-rest-api-openapi.yml
operations:
  - searchDocuments
  - SearchAccountDocuments
  - getOrExportDocument
  - getDocumentContent
  - describeLink
generated: '2026-08-01'
method: generated
source: openapi/lucid-rest-api-openapi.yml
---

# Search and export Lucid documents

Base URL `https://api.lucid.co`.

## Steps

1. **Search.** `searchDocuments` (`POST /v1/documents/search`) takes a JSON body — not query
   parameters. Useful fields: `keywords` (truncated to 400 characters), `product`
   (`lucidchart` / `lucidspark` / `lucidscale`), `createdStartTime` / `createdEndTime`,
   `lastModifiedAfter` / `lastModifiedBefore`, `excludeTrashed`, `owners`, `documentIds`,
   `externalAccess`, `statusIds`. When `keywords` is supplied the results are sorted by relevance.
2. **Account-wide search** (admins) uses `SearchAccountDocuments`
   (`POST /v1/accounts/me/documents/search`).
3. **Read the structure.** `getDocumentContent` (`GET /v1/documents/{id}/contents`) returns the
   pages, shapes and lines — use this when the task is to reason about what a diagram *says*.
4. **Export a rendering.** `getOrExportDocument` (`GET /v1/documents/{id}`) with the `Accept`
   header set to the target format.
5. **Describe a pasted link.** `describeLink` (`POST /v1/describeLink`) unfurls a Lucid URL into
   title/preview metadata without opening the document.

## Rules

- Trashed documents are **included** by default; set `excludeTrashed: true` to drop them.
- `owners` and `documentIds` are capped at 10,000 entries each.
- Passing a `product` whose readonly scope the token lacks returns `403`, not an empty result.
- Search results are not cursor-paginated; only the audit-log endpoints use `pageSize`/`pageToken`.
