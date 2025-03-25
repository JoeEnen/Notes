
# Group Clause
Table:

| Transaction ID | amount | Customer ID |
|---------------|--------|-------------|
| 1000          | 4.9    | 3           |
| 1001          | 2.8    | 2           |
| 1002          | 3.3    | 3           |
| 1003          | 4.9    | 1           |
| 1004          | 1.0    | 4           |

## Using Aggregate Functions with GROUP BY

You can use aggregate functions with the GROUP BY clause to summarize data for each group.

The results based on a specific column

Example: Find the average salary for each department.

```sql
SELECT customer_id, SUM(amount) AS total_spent
FROM transactions
GROUP BY customer_id;

```
Output:

| customer_id | total_spent |
|------------|------------|
| 1          | 4.9        |
| 2          | 2.8        |
| 3          | 8.2        |
| 4          | 1.0        |



## Using Aggregate Functions with WHERE and HAVING

### Where
*WHERE* filters rows before aggregation.


*Calculate Total Amount for Transactions Above 2.0*

```sql
SELECT customer_id, SUM(amount) AS total_spent
FROM transactions
WHERE amount > 2.0
GROUP BY customer_id;

```
 Output:

 | customer_id | total_spent |
|------------|------------|
| 1          | 4.9        |
| 2          | 2.8        |
| 3          | 8.2        |


### Having
*HAVING* filters aggregated results.

*Customers Who Spent More Than 4.0*

```sql
SELECT customer_id, SUM(amount) AS total_spent
FROM transactions
GROUP BY customer_id
HAVING SUM(amount) > 4.0;
```
Output;

| customer_id | total_spent |
|------------|------------|
| 1          | 4.9        |
| 3          | 8.2        |



