Top 50 SQL Queries Asked in Interviews

> Practical, job-ready queries with short explanations. Crack interviews, not textbooks.




---

1. Select all records from a table

SELECT * FROM employees;

Explanation: Basic fetch of all rows and columns.


---

2. Select specific columns

SELECT name, salary FROM employees;

Explanation: Only fetch selected fields.


---

3. Filter with WHERE clause

SELECT * FROM employees WHERE salary > 50000;

Explanation: Fetch rows matching a condition.


---

4. AND / OR conditions

SELECT * FROM employees WHERE department = 'HR' AND salary > 40000;

Explanation: Combine multiple conditions.


---

5. Sorting results

SELECT * FROM employees ORDER BY salary DESC;

Explanation: Sort results by column (descending).


---

6. Aggregate with GROUP BY

SELECT department, COUNT(*) FROM employees GROUP BY department;

Explanation: Count records per department.


---

7. GROUP BY with HAVING

SELECT department, AVG(salary) 
FROM employees 
GROUP BY department 
HAVING AVG(salary) > 50000;

Explanation: Filter after grouping.


---

8. INNER JOIN two tables

SELECT e.name, d.name AS department_name 
FROM employees e 
JOIN departments d ON e.department_id = d.id;

Explanation: Match records from both tables.


---

9. LEFT JOIN

SELECT e.name, d.name 
FROM employees e 
LEFT JOIN departments d ON e.department_id = d.id;

Explanation: Include all from left table, even unmatched.


---

10. Subquery in WHERE

SELECT name FROM employees 
WHERE salary > (SELECT AVG(salary) FROM employees);

Explanation: Compare each row with an aggregate.


---

11. Find duplicate values

SELECT email, COUNT(*) 
FROM users 
GROUP BY email 
HAVING COUNT(*) > 1;

Explanation: Group and filter repeated values.


---

12. Get the second highest salary

SELECT MAX(salary) 
FROM employees 
WHERE salary < (SELECT MAX(salary) FROM employees);

Explanation: Nested query to find 2nd highest.


---

13. Find employees without managers

SELECT name FROM employees 
WHERE manager_id IS NULL;

Explanation: Handle NULL values.


---

14. Get top 3 salaries

SELECT DISTINCT salary 
FROM employees 
ORDER BY salary DESC 
LIMIT 3;

Explanation: Use LIMIT to restrict result count.


---

15. Update a record

UPDATE employees 
SET salary = 60000 
WHERE name = 'Pooja';

Explanation: Modify existing record.


---

16. Delete a record

DELETE FROM employees 
WHERE name = 'Simba';

Explanation: Remove specific record.


---

17. Insert a new record

INSERT INTO employees (name, salary, department) 
VALUES ('Bhaskar', 70000, 'IT');

Explanation: Add a new row.


---

18. Find highest salary per department

SELECT department, MAX(salary) 
FROM employees 
GROUP BY department;

Explanation: Combine aggregate and group.


---

19. Count total records

SELECT COUNT(*) FROM employees;

Explanation: Total number of rows.


---

20. Rename a table

RENAME TABLE old_table TO new_table;

Explanation: Change table name.


---

21. Change a column name

ALTER TABLE employees RENAME COLUMN name TO full_name;

Explanation: Rename a column.


---

22. Add a new column

ALTER TABLE employees ADD birthdate DATE;

Explanation: Add a new column to table.


---

23. Delete a column

ALTER TABLE employees DROP COLUMN birthdate;

Explanation: Remove a column.


---

24. Create a new table

CREATE TABLE departments (
  id INT PRIMARY KEY,
  name VARCHAR(50)
);

Explanation: Define a new table schema.


---

25. Drop a table

DROP TABLE departments;

Explanation: Permanently remove a table.


---

26. Truncate a table

TRUNCATE TABLE employees;

Explanation: Delete all data, keep structure.


---

27. Find NULL values

SELECT * FROM employees WHERE email IS NULL;

Explanation: Find missing entries.


---

28. NOT NULL filter

SELECT * FROM employees WHERE email IS NOT NULL;

Explanation: Filter out missing values.


---

29. BETWEEN clause

SELECT * FROM employees WHERE salary BETWEEN 40000 AND 60000;

Explanation: Select range values.


---

30. IN clause

SELECT * FROM employees WHERE department IN ('HR', 'Finance');

Explanation: Filter for multiple exact values.


---

31. NOT IN clause

SELECT * FROM employees WHERE department NOT IN ('HR', 'Finance');

Explanation: Exclude certain values.


---

32. LIKE clause

SELECT * FROM employees WHERE name LIKE 'P%';

Explanation: Pattern matching (starts with P).


---

33. Wildcard match with % and _

SELECT * FROM employees WHERE name LIKE '_ooja';

Explanation: Match pattern with single char placeholder (_).


---

34. DISTINCT values

SELECT DISTINCT department FROM employees;

Explanation: Get unique values only.


---

35. LIMIT rows

SELECT * FROM employees LIMIT 5;

Explanation: Restrict number of rows.


---

36. OFFSET usage

SELECT * FROM employees LIMIT 5 OFFSET 5;

Explanation: Skip first 5 rows.


---

37. Check existence of rows

SELECT EXISTS (SELECT 1 FROM employees WHERE salary > 100000);

Explanation: Returns true/false if any matching row exists.


---

38. UNION two queries

SELECT name FROM employees 
UNION 
SELECT name FROM managers;

Explanation: Combine unique rows from both queries.


---

39. UNION ALL

SELECT name FROM employees 
UNION ALL 
SELECT name FROM managers;

Explanation: Combine all rows, including duplicates.


---

40. CASE statement (IF/ELSE logic)

SELECT name, 
  CASE 
    WHEN salary > 70000 THEN 'High'
    ELSE 'Average'
  END AS salary_level
FROM employees;

Explanation: Add condition-based values.


---

41. COALESCE (fallback value)

SELECT name, COALESCE(email, 'no-email@example.com') FROM employees;

Explanation: Replace NULL with default.


---

42. ROUND a number

SELECT ROUND(salary, 2) FROM employees;

Explanation: Round salary to 2 decimal places.


---

43. MOD function

SELECT name FROM employees WHERE MOD(id, 2) = 0;

Explanation: Filter even numbered IDs.


---

44. String concatenation

SELECT CONCAT(first_name, ' ', last_name) AS full_name FROM employees;

Explanation: Combine columns as one string.


---

45. Current date/time

SELECT CURRENT_DATE, CURRENT_TIME, NOW();

Explanation: Fetch current date/time values.


---

46. Extract year from date

SELECT EXTRACT(YEAR FROM join_date) FROM employees;

Explanation: Get year from a date column.


---

47. Convert text to lowercase or uppercase

SELECT UPPER(name), LOWER(name) FROM employees;

Explanation: Format text casing.


---

48. Find length of text

SELECT LENGTH(name) FROM employees;

Explanation: Count characters in a string.


---

49. Alias for columns or tables

SELECT e.name FROM employees e;

Explanation: Use alias to shorten references.


---

50. Comment inside SQL

-- This is a comment
SELECT * FROM employees;  /* Inline comment */

Explanation: Add notes in queries.



