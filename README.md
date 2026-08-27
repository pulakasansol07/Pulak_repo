# SQL Interview Prep

A collection of common SQL interview questions with detailed answers and sample queries.  
This repository is designed to help candidates strengthen their database fundamentals.

---

## 📖 Topics Covered
- Difference between `WHERE` and `HAVING`
- Handling of `NULL` values in aggregate functions
- Aggregate functions for totals and averages
- Using aggregate functions without `GROUP BY`

---

## 1. Difference between WHERE and HAVING
- **WHERE** filters rows before grouping/aggregation.
- **HAVING** filters groups after aggregation.

```sql
-- WHERE example
SELECT * 
FROM Employees 
WHERE Salary > 50000;

-- HAVING example
SELECT Department, AVG(Salary) AS AvgSalary
FROM Employees
GROUP BY Department
HAVING AVG(Salary) > 60000;
