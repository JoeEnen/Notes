# Aggregate Functions in Databases

Aggregate functions in databases are used to perform calculations on a set of values and return a single summarized result. They are commonly used in reports, data analysis, and statistics.

These functions work with multiple rows but return one output.

# Types of Aggregate Functions

## 1. COUNT() – Counting Records

The COUNT() function is used to count the number of rows in a table or the number of non-null values in a column.

🔹 Syntax:
```sql
SELECT COUNT(*) FROM employees;
```

🔹 Example Output:

COUNT(*)
50
## 2. SUM() – Adding Values
The SUM() function calculates the total sum of a numeric column.

🔹 Syntax:

 ```sql
SELECT SUM(salary) FROM employees;
```
🔹 Example Output:

SUM(salary)
1,200,000
Tip: Works only with numeric columns.

## 3.AVG() – Calculating Average
The AVG() function calculates the average (mean) value of a numeric column.

🔹 Syntax:
```sql
SELECT AVG(salary) FROM employees;
```

🔹 Example Output:

AVG(salary)
24,000

 Tip: Ignores NULL values when calculating the average.

## 4. MIN() – Finding the Smallest Value
The MIN() function returns the lowest value in a column.

🔹 Syntax:

sql
Copy
Edit
SELECT MIN(salary) FROM employees;
🔹 Example Output:

MIN(salary)
15,000

## 5.MAX() – Finding the Largest Value
 The MAX() function returns the highest value in a column.

🔹 Syntax:

```sql
SELECT MAX(salary) FROM employees;
```
Example Output:

MAX(salary)
50,000

# Using Aggregate Functions with GROUP BY

You can use aggregate functions with the GROUP BY clause to summarize data for each group.

Example: Find the average salary for each department.

```sql
Copy
Edit
SELECT department, AVG(salary) 
FROM employees
GROUP BY department;
```

Example Output:

Department	AVG(salary)
HR	20,000
IT	30,000
Marketing	25,000

# Using Aggregate Functions with WHERE and HAVING
WHERE filters rows before aggregation.

HAVING filters aggregated results.

🔹 Example: Get the total salary for departments where total salary exceeds 100,000.
```sql
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/JoeEnen/Notes.git
git push -u origin main
```