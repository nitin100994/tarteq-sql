Top 20 SQL Queries Asked in Interviews

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

✅ You're now interview-ready. Copy these, tweak them, and own the room.

