# Engineering case studies

Real production issues I investigated and solved, written up as case studies. Details are anonymized.

- **L3 – Production incident:** prod impact, plus a prod data repair, cross-team coordination or a risky call under pressure.
- **L2 – Cross-cutting:** spans services or messaging, concurrency, transactions, EF Core or performance, or needs a data repair.
- **L1 – Focused fix:** one service, root cause in its own code or query, no data repair.

## L3 – Production incidents

| # | Case | Tags | Hook |
|---|------|------|------|
| 002 | [Release blocked by a unique index on dirty data](cases/002-unique-index-migration-blocked-by-duplicates.md) | EF Core · Migrations · SQL Server · Release management · Prod incident | A unique index passed on clean staging and blocked prod; I chose to unblock with a weaker index and turn a risky data merge into a planned follow-up |

## L2 – Cross-cutting issues

| # | Case | Tags | Hook |
|---|------|------|------|
| 001 | [Offer prices show zero after bid opening](cases/001-api-instance-hijacks-message-retries.md) | Microservices · Kafka/CAP · Message retries · Data repair | An API with no subscribers silently stole a worker's message retries; the retry count, not the error text, gave it away |

## L1 – Focused fixes

_None yet._
