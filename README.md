# SQL Fundamentals — Session 1: Filtering & Aggregation

First in a series of SQL practice sessions working with a telecom-style `customer` and `billing` dataset. Covers the basics of querying and filtering relational data.

**Covers:** `SELECT` / `DESCRIBE`, column filtering, `DISTINCT`, `WHERE` with `IN`, pattern matching with `LIKE` and wildcards, `ORDER BY`, `LIMIT`, aggregate functions (`COUNT`, `SUM`).

## Example

```sql
-- unique emails, and a count of them
SELECT DISTINCT email FROM customer;
SELECT COUNT(DISTINCT email) FROM customer;

-- pattern matching: numbers starting with 277, addresses among a list
SELECT * FROM customer
WHERE address IN ("5 Northridge Road", "814 Kinsman Lane")
  AND phone_number LIKE "277%";
```

## Files

- `Customer.csv`, `Billing.csv` — sample dataset
- Query script (see repository)

## Note

This is part of a progressive series (Sessions 1–6) building up SQL skills on the same dataset — see Sessions 2–6 for DDL, joins, subqueries, window functions, and CTEs.
