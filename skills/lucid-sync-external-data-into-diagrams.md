---
name: Sync external data into Lucid diagrams
description: Push structured data into Lucid with the Data API — create a data source, a collection and its field-definition schema, then upsert data items that shape-data and formula-driven shapes bind to.
api: openapi/lucid-data-api-openapi.yml
operations:
  - createDataSource
  - createDataSourceFromCSV
  - createCollection
  - updateFieldDefinitions
  - createDataItems
  - updateDataItemsByKey
  - getAllDataItems
  - getRateLimits
generated: '2026-08-01'
method: generated
source: openapi/lucid-data-api-openapi.yml
---

# Sync external data into Lucid diagrams

Base URL `https://data.lucid.app`. OAuth 2.0 only, and a single scope covers the whole surface:
`data-service.admin`.

## Steps

1. **Create the data source.** `createDataSource` (`POST /dataSources`) — the container for one
   external system. For a one-shot file load use `createDataSourceFromCSV` (`POST /adapter/csv`)
   and `updateDataSourceFromCSV` (`PUT /adapter/csv`) to refresh it.
2. **Create a collection.** `createCollection` (`POST /collections`) — a collection is the table.
3. **Define the schema.** `updateFieldDefinitions` (`PATCH /collections/{collectionId}/schema`)
   declares the fields. `getAllFieldDefinitions` reads them back;
   `updateFieldDefinition` / `deleteFieldDefinition` operate on a single field.
4. **Load rows.** `createDataItems` (`POST /collections/{collectionId}/items`), then
   `updateDataItems` / `deleteDataItems`. When your system has its own primary key, use the
   by-key variants — `getDataItemsByKey`, `updateDataItemsByKey`, `deleteDataItemsByKey` — so you
   do not have to store Lucid's item ids.
5. **Read back.** `getAllDataItems` with `start` / `end` / `fields` / `filter`;
   `getTotalDataItemsCount` (`HEAD /collections/{collectionId}/items`) for the count alone.
6. **Share it.** `createDataSetGrant` (`POST /dataSetGrants`) grants another account or user
   access to a data set.

## Rules

- **Check your budget first.** `getRateLimits` (`GET /rateLimits`) returns the live
  `userApiCallRate` (750 requests/minute), `userHardRefreshInterval` and `userSoftRefreshInterval`
  (30 seconds each) and `fileSizeLimit` (3 MB). Honour the refresh intervals — a hard refresh
  triggered inside the window is rejected, not queued.
- CSV uploads above the reported `fileSizeLimit` fail; split the file.
- The Data API declares no `components.schemas` — request and response shapes are inline in each
  operation. Read the operation, not a shared model.
- No idempotency key: use the by-key upsert operations rather than retrying `createDataItems`.
