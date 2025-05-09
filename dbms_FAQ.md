DBMS Basics – For Interviews, Learning & Love

> Explained like you're 5, but preparing like you're 25. Emojis, examples, diagrams, and chill logic ahead.




---

1. What is DBMS?

DBMS = Database Management System

It's a software to store, manage, and retrieve data.


Examples: MySQL, Oracle, PostgreSQL, SQLite, MongoDB

Imagine: A magical notebook where Simba writes all snack timings, and Bhaskar retrieves it when needed.


---

2. DBMS vs RDBMS

RDBMS = Relational DBMS (uses relations/tables) ✅


---

3. Types of Keys

Primary Key – Unique & Not Null (e.g., roll_no)

Foreign Key – Refers to a Primary Key in another table

Candidate Key – All possible unique keys (one becomes primary)

Composite Key – Combination of two columns used as key

Super Key – Primary Key + other attributes that uniquely identify a row


Diagram:

+------------+----------+-----------------------+
| roll_no (PK)| name     | email (Candidate Key) |
+------------+----------+-----------------------+
| 101        | Arya     | arya@mail.com         |
| 102        | Pooja    | pooja@mail.com        |
+------------+----------+-----------------------+


---

4. Normalization

1NF – Atomic values only

Bad: {phone: 9876, 1234}   ✅ Good: {phone1: 9876, phone2: 1234}

2NF – No partial dependency

If PK = (roll_no, course_id) → all columns must depend on both

3NF – No transitive dependency

If A → B and B → C, then A → C must not exist (unless C is a key)

Real-life: Instead of writing "Pooja - Delhi - India" repeatedly, normalize them into city & country tables.


---

5. ER Model (Entity Relationship)

Diagram (Text version):

[Student] ---- borrows ---- [Book]
   |                          |
 [roll_no, name]         [id, title]

Cardinalities:

1:1 → Husband – Wife

1:M → Teacher – Students

M:N → Students – Courses


Symbols (when drawing):

Rectangle = Entity

Oval = Attribute

Diamond = Relationship



---

6. ACID Properties

Diagram:

+------------+-------------+-----------------+--------------+
| Atomicity  | Consistency | Isolation       | Durability   |
+------------+-------------+-----------------+--------------+
| All-or-none| Always valid| Acts independently| Once done, stays done |
+------------+-------------+-----------------+--------------+

Example: Sending ₹500 to Simba’s bank account. All 4 properties must hold!


---

7. Indexing

Diagram (Conceptual):

Book Table of Contents = Index
Instead of flipping 500 pages, jump directly to pg 132 for "Hash Joins"

Clustered Index → Rearranges actual table

Non-Clustered → Creates pointer-based lookup



---

8. Joins Conceptually

Table A: Students      Table B: Courses
+----+--------+        +----+----------+
| id | name   |        | id | title    |
+----+--------+        +----+----------+
| 1  | Pooja  |        | 1  | SQL      |
| 2  | Arya   |        | 2  | Python   |

INNER JOIN = Matching ids only (students enrolled) LEFT JOIN = All students, courses if exist


---

9. Concurrency & Locking

Multiple users = concurrency

Lock prevents clash (Read/Write locks)

Deadlock: Both wait on each other forever


User A locks Table 1
User B locks Table 2
→ Both need each other’s tables = deadlock


---

10. Backup & Recovery

Backup = Save current state

Recovery = Load backup after failure


Tip: Automate Simba’s snack schedule backup every night!


---

⚡️ MCQs – Interview Style

Q1: Which key can have duplicate values?

A. Primary Key

B. Foreign Key ✅

C. Candidate Key

D. Super Key


Q2: Which normal form eliminates transitive dependencies?

A. 1NF

B. 2NF

C. 3NF ✅

D. 4NF


Q3: What does ACID stand for?

A. Automated, Compiled, Indexed, Distributed

B. Atomicity, Consistency, Isolation, Durability ✅


Q4: Which JOIN includes unmatched rows from the left table?

A. INNER

B. LEFT ✅

C. RIGHT

D. CROSS


Q5: Which index stores data sorted by key?

A. Hash

B. Clustered ✅

C. Non-clustered

D. Composite



---

❓ FAQ – Asked in Interviews

Q: Why do we need normalization? A: To avoid data redundancy, update anomalies, and improve integrity.

Q: When would you denormalize a DB? A: For faster reads in analytics, when duplication is acceptable.

Q: What’s the difference between Primary and Unique Key? A: Both ensure uniqueness. Primary = only one per table & can’t be NULL.

Q: Can a table have multiple foreign keys? A: Yes. Each refers to different parent tables.

Q: What happens during rollback? A: Any incomplete transaction is undone – database returns to safe state.


---

✅You’re now theory-rich, visually wired, and MCQ-tested.

