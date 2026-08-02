---
name: Provision Lucid users and groups with SCIM 2.0
description: Create, update, search and deprovision Lucid users and groups/teams from an identity provider using the SCIM 2.0 API.
api: openapi/lucid-scim-api-openapi.yml
operations:
  - getAllUsers
  - createUser
  - getUser
  - modifyUserPut
  - modifyUserPatch
  - deleteUser
  - getAllGroups
  - createGroup
  - modifyGroupPatch
  - deleteGroup
  - getServiceProviderConfig
generated: '2026-08-01'
method: generated
source: openapi/lucid-scim-api-openapi.yml
---

# Provision Lucid users and groups with SCIM 2.0

Base URL `https://users.lucid.app/scim/v2`. Bearer-token auth (`Bearer` security scheme).
Enterprise accounts only.

## Steps

1. **Confirm capability.** `getServiceProviderConfig` (`GET /ServiceProviderConfig`) reports which
   SCIM features this tenant supports before you branch on PATCH vs PUT.
2. **Find the user.** `getAllUsers` (`GET /Users`) with `filter` (SCIM filter syntax),
   `startIndex` and `count`. Use `attributes` / `excludedAttributes` to trim the payload.
3. **Create.** `createUser` (`POST /Users`). A duplicate returns `409`.
4. **Update.** Prefer `modifyUserPatch` (`PATCH /Users/{id}`) for partial changes;
   `modifyUserPut` (`PUT /Users/{id}`) replaces the resource.
5. **Deprovision.** `deleteUser` (`DELETE /Users/{id}`).
6. **Groups and teams** mirror the same shape: `getAllGroups`, `createGroup`, `modifyGroupPatch`,
   `modifyGroupPut`, `deleteGroup`. In Lucid a SCIM Group maps to a Lucid team.

## Rules

- SCIM here is genuinely SCIM 2.0 — `urn:ietf:params:scim:*` schemas, `/Schemas` introspection,
  index-based pagination. Do not invent Lucid-specific query parameters.
- `401` is declared on **every** SCIM operation; `409` on create/modify means a conflicting
  userName or externalId.
- One operation declares `424` (failed dependency) — treat it as retryable only after resolving
  the referenced resource.
- The SCIM host rejects unauthenticated requests to every path with `403`, including
  `/.well-known/*`.
