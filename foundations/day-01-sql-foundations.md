# SQL Practice — Day 1: Query Foundations

**Date:** 2026-09-12  
**Track:** Backend Engineering + AI Engineering  
**Database dialect:** PostgreSQL  
**Status:** In progress

## Learning objectives

- Understand tables, rows, columns, and primary keys.
- Select specific columns with `SELECT`.
- Filter rows using `WHERE`.
- Combine conditions with `AND`, `OR`, and `IN`.
- Filter numeric ranges using `BETWEEN`.
- Handle missing values with `IS NULL` and `IS NOT NULL`.
- Sort results using `ORDER BY`.
- Restrict output with `LIMIT`.
- Remove duplicate results with `DISTINCT`.

## Practice dataset

### `employees`

| employee_id | employee_name | department | salary | manager_id |
|---:|---|---|---:|---:|
| 101 | Amit | Engineering | 90000 | 201 |
| 102 | Neha | Finance | 75000 | 202 |
| 103 | Rahul | Engineering | 110000 | NULL |
| 104 | Sara | HR | 70000 | 202 |

## Core concepts

- A **table** is a collection of related data.
- A **row** represents one record.
- A **column** represents one attribute of every record.
- A **primary key** uniquely identifies each row.
- `WHERE` filters rows.
- `ASC` sorts from lowest to highest or A to Z.
- `DESC` sorts from highest to lowest or Z to A.
- `NULL` means missing or unknown; test it using `IS NULL`, not `= NULL`.
- `BETWEEN` includes both boundary values.

## Completed exercises

### 1. Select specific columns

```sql
SELECT employee_id, employee_name, department
FROM employees;
```

### 2. Filter by department

```sql
SELECT employee_name, salary
FROM employees
WHERE department = 'Engineering';
```

### 3. Filter by salary and sort descending

```sql
SELECT employee_name, department, salary
FROM employees
WHERE salary > 80000
ORDER BY salary DESC;
```

### 4. Combine department and salary conditions

```sql
SELECT employee_name, department, salary
FROM employees
WHERE department IN ('Engineering', 'Finance')
  AND salary >= 80000
ORDER BY salary DESC;
```

### 5. Filter an inclusive salary range

```sql
SELECT employee_name, salary
FROM employees
WHERE salary BETWEEN 75000 AND 100000
ORDER BY salary ASC;
```

**Correction learned:** The original attempt used `DESC`, but the requirement was lowest to highest, which requires `ASC`.

### 6. Find rows containing a missing value

```sql
SELECT employee_name
FROM employees
WHERE manager_id IS NULL;
```

### 7. Return the top two employees who have managers

```sql
SELECT employee_name, salary
FROM employees
WHERE manager_id IS NOT NULL
ORDER BY salary DESC
LIMIT 2;
```

### 8. Return unique qualifying departments

```sql
SELECT DISTINCT department
FROM employees
WHERE salary >= 75000
ORDER BY department ASC;
```

**Correction learned:** Alphabetical A-to-Z ordering requires `ASC`; `DESC` produces Z-to-A ordering.

## Final Day 1 challenge

Write one query that returns:

- `employee_name`
- `department`
- `salary`

Requirements:

1. The department must be Engineering or Finance.
2. The employee must have a manager.
3. Salary must be between ₹70,000 and ₹100,000, inclusive.
4. Sort from highest to lowest salary.
5. Return only the first two employees.

```sql
-- Write the final answer here before checking it later.

```

## Progress log

| Skill | Status | Notes |
|---|---|---|
| Selecting columns | Completed | Correct |
| Text filtering | Completed | Correct |
| Numeric filtering | Completed | Correct |
| `AND`, `OR`, and `IN` | Completed | Correct |
| `BETWEEN` | Completed | Filtering correct |
| `NULL` handling | Completed | Correct |
| `LIMIT` | Completed | Correct |
| `DISTINCT` | Completed | Correct |
| Sort direction | Review needed | Recheck `ASC` versus `DESC` |
| Final challenge | Pending | Complete before Day 2 |

## Day 1 takeaway

Before executing a query, translate the requirement into this sequence:

1. Which table contains the data?
2. Which columns should be displayed?
3. Which rows should be included?
4. In what order should they appear?
5. Should the number of returned rows be limited?
