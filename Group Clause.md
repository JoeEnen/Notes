
# Group Clause
## Using Aggregate Functions with GROUP BY

You can use aggregate functions with the GROUP BY clause to summarize data for each group.

Example: Find the average salary for each department.

```sql
SELECT department, AVG(salary) 
FROM employees
GROUP BY department;
```

Example Output:

| Department  | AVG(salary) |
|------------|-------------|
| HR         | 20,000      |
| IT         | 30,000      |
| Marketing  | 25,000      |


## Using Aggregate Functions with WHERE and HAVING

*WHERE* filters rows before aggregation.

*HAVING* filters aggregated results.

Example: Get the total salary for departments where total salary exceeds 100,000.

```sql
 SELECT department, SUM(salary) 
FROM employees
GROUP BY department
HAVING SUM(salary) > 100000;
```