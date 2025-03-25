# Aggregate Functions in Databases

Aggregate functions in databases are used to perform calculations on a set of values and return a single summarized result. They are commonly used in reports, data analysis, and statistics.

These functions work with multiple rows but return one output.

# Types of Aggregate Functions

## 1. COUNT() – Counting Records

The COUNT() function is used to count the number of rows in a table or the number of non-null values in a column.


```sql
SELECT COUNT(*) FROM employees;
```

🔹 Example Output:

COUNT(*)

50

## 2. SUM() – Adding Values
The SUM() function calculates the total sum of a numeric column.



 ```sql
SELECT SUM(salary) FROM employees;
```
Example Output:

SUM(salary)

1,200,000

Note: Works only with numeric columns.

## 3.AVG() – Calculating Average
The AVG() function calculates the average (mean) value of a numeric column.


```sql
SELECT AVG(salary) FROM employees;
```

Example Output:

AVG(salary)
24,000

 Note: Ignores NULL values when calculating the average.

## 4. MIN() – Finding the Smallest Value
The MIN() function returns the lowest value in a column.

```sql
SELECT MIN(salary) FROM employees;
```

Example Output:

MIN(salary)
15,000

## 5.MAX() – Finding the Largest Value
 The MAX() function returns the highest value in a column.


```sql
SELECT MAX(salary) FROM employees;
```
Example Output:

MAX(salary)
50,000
