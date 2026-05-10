# sql-fundamentals.md

# SQL Fundamentals

## What is SQL?

SQL (Structured Query Language) is a language used to communicate with relational databases.

It allows users to:

- Retrieve data
- Filter data
- Sort data
- Aggregate data
- Modify data

SQL is one of the most important tools in Data Science, Data Analysis, and Backend Development.

---

# Database Concepts

## Database

A database is an organized collection of data.

Example:

| id  | name | age |
| --- | ---- | --- |
| 1   | John | 25  |
| 2   | Emma | 30  |

---

## Table

A table stores data in rows and columns.

- Rows → records
- Columns → attributes/features

---

## Primary Key

A primary key uniquely identifies each row in a table.

Example:

```sql
id
```

Each value must be unique.

---

# SELECT Statement

## Purpose

Used to retrieve data from a table.

## Syntax

```sql
SELECT column_name
FROM table_name;
```

## Example

```sql
SELECT name, age
FROM employees;
```

## Explanation

This query retrieves the name and age columns from the employees table.

---

# SELECT ALL

## Syntax

```sql
SELECT *
FROM table_name;
```

## Example

```sql
SELECT *
FROM employees;
```

## Explanation

Retrieves all columns from the table.

---

# WHERE Clause

## Purpose

Used to filter rows based on conditions.

## Syntax

```sql
SELECT column_name
FROM table_name
WHERE condition;
```

## Example

```sql
SELECT *
FROM employees
WHERE age > 25;
```

## Explanation

Returns employees whose age is greater than 25.

---

# Comparison Operators

| Operator | Meaning               |
| -------- | --------------------- |
| =        | Equal                 |
| !=       | Not equal             |
| >        | Greater than          |
| <        | Less than             |
| >=       | Greater than or equal |
| <=       | Less than or equal    |

---

# AND / OR Operators

## AND

Both conditions must be true.

```sql
SELECT *
FROM employees
WHERE age > 25 AND salary > 5000;
```

---

## OR

At least one condition must be true.

```sql
SELECT *
FROM employees
WHERE department = 'IT' OR department = 'HR';
```

---

# ORDER BY

## Purpose

Used to sort query results.

## Syntax

```sql
SELECT *
FROM table_name
ORDER BY column_name;
```

## Example

```sql
SELECT *
FROM employees
ORDER BY salary DESC;
```

## Explanation

Sorts employees by salary from highest to lowest.

---

# LIMIT

## Purpose

Used to limit the number of returned rows.

## Example

```sql
SELECT *
FROM employees
LIMIT 5;
```

## Explanation

Returns only the first 5 rows.

---

# LIKE Operator

## Purpose

Used for pattern matching.

## Example

```sql
SELECT *
FROM employees
WHERE name LIKE 'J%';
```

## Explanation

Returns employees whose names start with the letter J.

---

# IN Operator

## Purpose

Used to check multiple possible values.

## Example

```sql
SELECT *
FROM employees
WHERE department IN ('IT', 'HR');
```

## Explanation

Returns employees working in IT or HR departments.

---

# BETWEEN Operator

## Purpose

Used to filter values within a range.

## Example

```sql
SELECT *
FROM employees
WHERE salary BETWEEN 3000 AND 7000;
```

## Explanation

Returns employees whose salary is between 3000 and 7000.
