📘 Day 15 – SQL Basics
=======================


✅ What I learned today

1. CRUD Operations
   ----------------

INSERT → INSERT INTO table (cols) VALUES (values)

SELECT → SELECT * FROM table WHERE condition

UPDATE → UPDATE table SET col=value WHERE condition

DELETE → DELETE FROM table WHERE condition


2. Filtering & Sorting
   --------------------

-> WHERE, AND/OR, BETWEEN, LIKE

-> ORDER BY col DESC/ASC

-> LIMIT n


3. Joins
   ------

-> INNER JOIN → matching records from both tables

-> LEFT JOIN → all from left, matching from right

// sql Query

SELECT e.name, d.dept_name

FROM employees e

INNER JOIN departments d ON e.department = d.dept_name;


4. Aggregates & Grouping
   ----------------------

-> COUNT(), SUM(), AVG(), MAX(), MIN()

-> GROUP BY → group by column

-> HAVING → filter after grouping

// sql Query

SELECT department, AVG(salary) AS avg_salary

FROM employees

GROUP BY department

HAVING AVG(salary) > 60000;


5. Practice Queries
   -----------------

// sql Query

-> Employees in IT

SELECT * FROM employees WHERE department = 'IT';

-> Average salary per department

SELECT department, AVG(salary) FROM employees GROUP BY department;

-> Highest salary per department

SELECT department, MAX(salary) FROM employees GROUP BY department;
