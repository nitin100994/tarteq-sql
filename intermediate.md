# **SQL Warm-Up Part 3: Joins, Aggregates & Subqueries – With Real-Life Vibes**  
> When Simba meets Bhaskar, or Pooja’s name pops up from a secret list — that’s SQL magic in action!

---

## 1. **INNER JOIN – Show Matches from Both Tables**  
```sql
SELECT e.name, d.name AS department_name 
FROM employees e 
JOIN departments d 
ON e.department_id = d.id;
```  
**Meaning:**  
🔗 *"Match employees with their department name, but only when there’s a valid match in both tables."*  
Like: *“Show students who have been assigned a class teacher.”*  
No class teacher, no show!

---

## 2. **LEFT JOIN – Keep Everyone from the Left Table**  
```sql
SELECT e.name, d.name AS department_name 
FROM employees e 
LEFT JOIN departments d 
ON e.department_id = d.id;
```  
**Meaning:**  
🧩 *"Show all employees. If someone has no department, leave it blank."*  
Like: *“List all kids—even those who haven’t been assigned a classroom yet.”*

---

## 3. **RIGHT JOIN – Focus on Right Table**  
```sql
SELECT e.name, d.name AS department_name 
FROM employees e 
RIGHT JOIN departments d 
ON e.department_id = d.id;
```  
**Meaning:**  
🧠 *"Show all departments and any employees in them. Even if no one is working in a department, still show it!"*  
Like: *“Show all class sections, even if they’re empty.”*

---

## 4. **FULL JOIN – Everyone’s Invited**  
```sql
SELECT e.name, d.name AS department_name 
FROM employees e 
FULL OUTER JOIN departments d 
ON e.department_id = d.id;
```  
**Meaning:**  
🌍 *"Show everything from both tables, matched or not."*  
Like: *“List all kids and all class sections, even if no match exists.”*

---

## 5. **Aggregates – Magic Math Functions**

### a. **COUNT – How Many?**
```sql
SELECT COUNT(*) FROM employees;
```  
🔢 *“How many total employees are there?”*

---

### b. **AVG – Average Salary**
```sql
SELECT AVG(salary) FROM employees;
```  
⚖️ *“What’s the average salary of all employees?”*

---

### c. **SUM – Add All Values**
```sql
SELECT SUM(salary) FROM employees;
```  
💰 *“How much salary do we pay in total every month?”*

---

### d. **MAX / MIN – Highest or Lowest**
```sql
SELECT MAX(salary) FROM employees;
```  
👑 *“Who earns the most?”*

```sql
SELECT MIN(salary) FROM employees;
```  
🐣 *“Who earns the least?”*

---

## 6. **GROUP BY – Create Mini Groups**  
```sql
SELECT department, COUNT(*) 
FROM employees 
GROUP BY department;
```  
📦 *"Count how many employees are in each department."*  
Like: *“How many kids in each class?”*

---

## 7. **HAVING – Condition on Grouped Data**  
```sql
SELECT department, AVG(salary) 
FROM employees 
GROUP BY department 
HAVING AVG(salary) > 50000;
```  
🎯 *“Show only those departments where average salary is more than ₹50,000.”*  
You’re now filtering the filtered!

--

## 8. **Subqueries – A Query Inside a Query**

### a. **Above Average Earners**
```sql
SELECT name 
FROM employees 
WHERE salary > (SELECT AVG(salary) FROM employees);
```  
🧙 *“List those who earn more than the average salary.”*

---
**Confused here I know me too so refer intermidiate.md**

### b. **Use Subquery in FROM**
```sql
SELECT dept, total 
FROM (
  SELECT department AS dept, COUNT(*) AS total 
  FROM employees 
  GROUP BY department
) AS dept_counts 
WHERE total > 5;
```  
🔍 *“Only show departments that have more than 5 employees.”*

---

### c. **Subquery in SELECT**
```sql
SELECT name, 
  (SELECT MAX(salary) FROM employees) AS highest_salary 
FROM employees;
```  
👀 *“For each person, also show the highest salary in the company.”*

**Confused here I know me too so refer intermidiate.md**

---

## ✨ Now You're Not Just a Beginner – You're Dangerous  
Joins, Aggregates, Subqueries – now in your toolkit.  
This is the stuff real developers and data wizards use.

Keep querying. Keep growing.

---