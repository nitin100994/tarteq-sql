# **SQL Queries for Beginners – Explained Like You're 5!**  
> Made with love for curious minds. Simple words, emojis, and examples!

---

## 1. **See Everything in a Table**  
```sql
SELECT * FROM employees;
```  
**Meaning:**  
📖 *"Show me everything in the notebook called employees."*  
Like reading the full attendance sheet of a class.

---

## 2. **See Only Specific Columns**  
```sql
SELECT name, salary FROM employees;
```  
**Meaning:**  
🎯 *"I only want names and salaries – not the whole report card!"*  
Simple and focused!

---

## 3. **Filter with a Condition (WHERE Clause)**  
```sql
SELECT * FROM employees WHERE salary > 50000;
```  
**Meaning:**  
🕵️ *"Only show people who earn more than ₹50,000."*  
Like: “Students who scored above 90 marks.”

---

## 4. **Use Multiple Conditions (AND / OR)**  
```sql
SELECT * FROM employees WHERE department = 'HR' AND salary > 40000;
```  
**Meaning:**  
🧠 *"Only show people in HR AND earning more than ₹40,000."*  
Like: “Show students from Class 10 AND scored above 90.”

---

## 5. **Sort the Results (ORDER BY)**  
```sql
SELECT * FROM employees ORDER BY salary DESC;
```  
**Meaning:**  
📊 *"Sort the list – highest salary comes first!"*  
Like arranging students by their marks, topper on top.

---

## 6. **Group and Count (GROUP BY)**  
```sql
SELECT department, COUNT(*) FROM employees GROUP BY department;
```  
**Meaning:**  
📦 *"How many people are in each department?"*  
Like: “How many students in each class?”

---

## 7. **Group with Condition (HAVING Clause)**  
```sql
SELECT department, AVG(salary) 
FROM employees 
GROUP BY department 
HAVING AVG(salary) > 50000;
```  
**Meaning:**  
🎯 *"Only show departments where average salary is more than ₹50,000."*  
Like: “Show classes where average marks are more than 90.”

---

## 8. **Join Two Tables (INNER JOIN)**  
```sql
SELECT e.name, d.name 
FROM employees e 
JOIN departments d ON e.department_id = d.id;
```  
**Meaning:**  
🔗 *"Match employees with their department name."*  
Like: “Match students with their class teachers.”

---

## 9. **Include Unmatched Data Too (LEFT JOIN)**  
```sql
SELECT e.name, d.name 
FROM employees e 
LEFT JOIN departments d ON e.department_id = d.id;
```  
**Meaning:**  
🧩 *"Show all employees – even those without departments."*  
Like: “List all students, even if we don’t know their class.”

---

## 10. **Subquery Magic (Query inside a Query)**  
```sql
SELECT name 
FROM employees 
WHERE salary > (SELECT AVG(salary) FROM employees);
```  
**Meaning:**  
🧙‍♂️ *"Find people who earn more than the average."*  
Like: “Students who scored above average.”

---

## ✨ The End (For Now...)  
SQL is like magic – just with logic!  
This is your beginner-friendly SQL spellbook.  
Keep practicing, and let the queries flow!

---