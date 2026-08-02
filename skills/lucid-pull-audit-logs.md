---
name: Pull Lucid audit logs
description: Page through the Lucid account audit log with cursor pagination, or query it with filters, for compliance and security monitoring.
api: openapi/lucid-rest-api-openapi.yml
operations:
  - getAuditLogs
  - queryAuditLogs
  - getAccountInformation
generated: '2026-08-01'
method: generated
source: openapi/lucid-rest-api-openapi.yml
---

# Pull Lucid audit logs

Base URL `https://api.lucid.co`. Requires the `account.audit.logs` scope
("View audit logs on your account").

## Steps

1. **Confirm the account.** `getAccountInformation` (`GET /v1/accounts/me`) returns the account id
   and name the logs belong to.
2. **Poll.** `getAuditLogs` (`GET /v1/auditLogs`) with `pageSize` and `pageToken`.
3. **Or filter.** `queryAuditLogs` (`POST /v1/auditLogs/query`) accepts a filter body and takes the
   same `pageSize` / `pageToken` query parameters.
4. **Follow the cursor.** Keep calling with the returned `pageToken` until no further token comes
   back. This is the **only** cursor-paginated surface in the Lucid REST API — everywhere else
   returns a bounded array.

## Rules

- Audit-log events are documented at
  https://developer.lucid.co/reference/audit-log-events — resolve event type names there rather
  than inferring them.
- Persist the last `pageToken` so a resumed poll does not re-read the window.
- No `Retry-After` header exists; on `429` back off and re-issue with the same `pageToken`.
