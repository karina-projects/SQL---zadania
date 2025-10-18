# PostgreSQL Practice Queries

This repository contains a set of SQL exercises and queries I used to practice PostgreSQL concepts.

## Covered topics
- Checking server configuration (`SHOW work_mem`, `SHOW timezone`, etc.)
- Working with dates and timestamps (`NOW()`, `CURRENT_DATE`, `TIMEOFDAY()`)
- Extracting data parts using `EXTRACT()`
- Calculating date differences with `AGE()`
- Formatting output using `TO_CHAR()`
- Using `TRIM()` to clean up text results
- Filtering and aggregating payments by weekday

## Example queries

```sql
-- Count how many payments happened on Monday
SELECT COUNT(*)
FROM payment
WHERE EXTRACT(DOW FROM payment_date) = 1;
