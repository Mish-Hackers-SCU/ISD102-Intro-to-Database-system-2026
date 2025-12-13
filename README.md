### <center><b>بسم الله الرحمن الرحيم</b></center>
------
![](msh_icon.png)

#𝔇𝔢𝔰𝔱𝔯𝔬𝔶 𝔱𝔥𝔢 𝔑𝔬𝔯𝔪𝔞𝔩#
------

**See different links to revise typing SQL queries:**
> [Oracle SQL Basics](https://www.oracletutorial.com/oracle-basics/) (Highly Recommended)

> [MySQL Basics](https://www.w3schools.com/mysql/default.asp)

> [SQL book]()
------

# 📖 Introduction to SQL

Welcome to the **Introduction to SQL** repository\! This resource is designed to provide a foundational understanding of Structured Query Language (SQL), focusing on core concepts and practical implementation using Oracle SQL syntax.

**ملحوظة:** الشرح المبسّط الموجود بين قوسين $(\dots)$ مكتوب باللهجة المصرية عشان يسهل عليك فهم المصطلحات التقنية.

## 🌟 Table of Contents

1.  [What is SQL?](https://www.google.com/search?q=%23what-is-sql)
2.  [SQL Command Categories (DDL, DML, DQL)](https://www.google.com/search?q=%23sql-command-categories-ddl-dml-dql)
3.  [Table Column Definitions](https://www.google.com/search?q=%23table-column-definitions)
      * [Datatypes](https://www.google.com/search?q=%23datatypes)
      * [Constraints](https://www.google.com/search?q=%23constraints)
          * [Unique](https://www.google.com/search?q=%23unique)
          * [NOT NULL](https://www.google.com/search?q=%23not-null)
          * [Primary Key](https://www.google.com/search?q=%23primary-key)
          * [Foreign Key](https://www.google.com/search?q=%23foreign-key)
          * [Primary Key vs. Foreign Key](https://www.google.com/search?q=%23primary-key-vs-foreign-key)
4.  [Table Creation and Data Manipulation](https://www.google.com/search?q=%23table-creation-and-data-manipulation)
      * [Creating a Table](https://www.google.com/search?q=%23creating-a-table)
      * [Inserting Values (DML)](https://www.google.com/search?q=%23inserting-values-dml)
      * [Modifying Table Structure (ALTER TABLE)](https://www.google.com/search?q=%23modifying-table-structure-alter-table)
      * [Deleting Data and Objects (DML & DDL)](https://www.google.com/search?q=%23deleting-data-and-objects-dml--ddl)
5.  [Data Querying (DQL)](https://www.google.com/search?q=%23data-querying-dql)
      * [The `SELECT` Statement](https://www.google.com/search?q=%23the-select-statement)
      * [`DISTINCT` and `FETCH`](https://www.google.com/search?q=%23distinct-and-fetch)
      * [The `WHERE` Clause](https://www.google.com/search?q=%23the-where-clause)
      * [Operators](https://www.google.com/search?q=%23operators)
      * [Aggregate Functions](https://www.google.com/search?q=%23aggregate-functions)
      * [`GROUP BY` and `ORDER BY`](https://www.google.com/search?q=%23group-by-and-order-by)
      * [`HAVING` and its Difference with `WHERE`](https://www.google.com/search?q=%23having-and-its-difference-with-where)
      * [`LIKE`, `IN`, `BETWEEN`](https://www.google.com/search?q=%23like-in-between)
      * [Column and Table Aliases](https://www.google.com/search?q=%23column-and-table-aliases)
      * [The `CASE` Expression](https://www.google.com/search?q=%23the-case-expression)
6.  [Joining Multiple Tables](https://www.google.com/search?q=%23joining-multiple-tables)
      * [Inner Join](https://www.google.com/search?q=%23inner-join)
      * [Full Outer Join](https://www.google.com/search?q=%23full-outer-join)
      * [Left and Right Outer Join](https://www.google.com/search?q=%23left-and-right-outer-join)
      * [Self Join](https://www.google.com/search?q=%23self-join)
7.  [Nested Queries (Subqueries)](https://www.google.com/search?q=%23nested-queries-subqueries)
8.  [Performance and Structure Tools](https://www.google.com/search?q=%23performance-and-structure-tools)
      * [Indexes](https://www.google.com/search?q=%23indexes)
      * [Views](https://www.google.com/search?q=%23views)

-----

## 1\. What is SQL?

**SQL** (Structured Query Language) is a standard language for managing data held in a Relational Database Management System (RDBMS). It is used to perform tasks such as updating, inserting, deleting, and retrieving data from a database.

$(\text{الـ SQL هي اللغة اللي بتكلمنا بيها الداتابيز. بتستخدم عشان ندخل بيانات، نعدلها، نمسحها، أو نطلع معلومات منها.})$

## 2\. SQL Command Categories (DDL, DML, DQL)

SQL commands are broadly categorized based on their function:

| Category | Full Form | Purpose | Example Commands |
| :--- | :--- | :--- | :--- |
| **DDL** | Data Definition Language | Defines, modifies, and deletes database objects (like tables, indexes, views). | `CREATE`, `ALTER`, `DROP` |
| **DML** | Data Manipulation Language | Manages data within schema objects. | `INSERT`, `UPDATE`, `DELETE` |
| **DQL** | Data Query Language | Used for retrieving data from the database. | `SELECT` |
| **TCL** | Transaction Control Language | Manages transactions (groups of DML statements). | `COMMIT`, `ROLLBACK` |

تقسيمة الأوامر:
الـ DDL بتلعب في هيكل الداتابيز (بتبني أو بتغير الجدول). الـ DML بتلعب في البيانات اللي جوه الجدول (بتضيف أو بتعدل صفوف). والـ DQL هي بتاعة الاستعلام بس).

## 3\. Table Column Definitions

### Datatypes

Datatypes define the type of data a column can hold (e.g., text, numbers, dates).

$(\text{نوع البيانات هو اللي بيحدد العمود ده هيشيل إيه: نصوص، أرقام، تواريخ... إلخ.})$

| Datatype (Oracle) | Description | Example Use |
| :--- | :--- | :--- |
| **`VARCHAR2(size)`** | Variable-length character string (text). | `NAME VARCHAR2(100)` |
| **`NUMBER(p, s)`** | Numeric value (p = precision, s = scale). | `SALARY NUMBER(8, 2)` |
| **`DATE`** | Stores date and time. | `HIRE_DATE DATE` |

### Constraints

Constraints enforce rules on the data columns to ensure data integrity.

$(\text{الـ Constraints دي قيود بنحطها على الأعمدة عشان نضمن إن البيانات اللي بتدخل الداتابيز تكون سليمة ومفيهاش لخبطة.})$

#### Unique

Ensures that all values in a column or a group of columns are different.

$(\text{بتخلي كل قيمة في العمود ده مكررتش قبل كده، كل صف لازم يكون ليه قيمة مختلفة.})$

```sql
CREATE TABLE Employees (
    employee_id NUMBER,
    email VARCHAR2(100) UNIQUE
);
```

#### NOT NULL

Ensures that a column cannot have a `NULL` value.

$(\text{العمود ده لازم يكون فيه قيمة، مينفعش يتساب فاضي } (\text{NULL}).)$

```sql
CREATE TABLE Employees (
    employee_id NUMBER,
    last_name VARCHAR2(50) NOT NULL
);
```

#### Primary Key

Uniquely identifies each row in a table. It is a combination of `UNIQUE` and `NOT NULL`.

$(\text{هو المفتاح الأساسي للجدول، زي رقم البطاقة كده، لازم يكون فريد ومينفعش يتساب فاضي. بنستخدمه للبحث السريع عن الصف.})$

```sql
CREATE TABLE Departments (
    dept_id NUMBER PRIMARY KEY,
    dept_name VARCHAR2(50) NOT NULL
);
```

#### Foreign Key

A column (or collection of columns) in one table that refers to the **Primary Key** in another table. It links two tables and maintains referential integrity.

$(\text{مفتاح في جدول بيشاور على الـ Primary Key في جدول تاني. هو اللي بيربط الجداول ببعض وبيخلي العلاقة بينهم سليمة.})$

```sql
CREATE TABLE Employees (
    employee_id NUMBER PRIMARY KEY,
    ...
    dept_id NUMBER,
    CONSTRAINT fk_dept
        FOREIGN KEY (dept_id)
        REFERENCES Departments(dept_id)
);
```

#### Primary Key vs. Foreign Key

| Feature | Primary Key (PK) | Foreign Key (FK) |
| :--- | :--- | :--- |
| **Purpose** | Uniquely identify a record (row) in a table. | Link two tables; enforce referential integrity. |
| **Constraint** | Must be **UNIQUE** and **NOT NULL**. | Can contain duplicates and *may* be NULL (unless specified otherwise). |
| **Table Count**| Only **one** PK per table. | A table can have **multiple** FKs. |

$(\text{الـ PK هو هوية الصف. الـ FK هو الكوبري اللي بيربط الجدول ده بجدول تاني.})$

## 4\. Table Creation and Data Manipulation

### Creating a Table

$(\text{بنبني هيكل الجدول وبنحدد الأعمدة وأنواعها والقيود اللي عليها.})$

```sql
CREATE TABLE Products (
    product_id NUMBER PRIMARY KEY,
    product_name VARCHAR2(100) NOT NULL,
    price NUMBER(6, 2),
    supplier_id NUMBER,
    CONSTRAINT fk_supplier
        FOREIGN KEY (supplier_id)
        REFERENCES Suppliers(supplier_id)
);
```

### Inserting Values (DML)

$(\text{بندخل بيانات جديدة (صفوف) جوه الجدول بعد ما عملناه.})$

```sql
INSERT INTO Products (product_id, product_name, price, supplier_id)
VALUES (101, 'Laptop', 1200.00, 50);
```

### Modifying Table Structure (ALTER TABLE)

#### Alter table modify columns

$(\text{بـ نغير مواصفات عمود موجود، زي نكبر حجمه أو نغير نوعه.})$

```sql
-- Increase the size of the product_name column
ALTER TABLE Products
MODIFY (product_name VARCHAR2(150));
```

#### Alter table add columns

$(\text{بـ نزود عمود جديد على الجدول الموجود.})$

```sql
-- Add a new column for product description
ALTER TABLE Products
ADD (product_description VARCHAR2(500));
```

### Deleting Data and Objects (DML & DDL)

| Command | Category | Purpose | Syntax |
| :--- | :--- | :--- | :--- |
| **`DELETE`** | DML | Removes **rows** from a table. Can be rolled back. | `DELETE FROM Products WHERE product_id = 101;` |
| **`TRUNCATE`** | DDL | Removes **all rows** from a table quickly. Cannot be rolled back. | `TRUNCATE TABLE Products;` |
| **`DROP`** | DDL | Permanently removes the **entire table structure** and data from the database. | `DROP TABLE Products;` |

$(\text{الـ DELETE بتمسح صفوف معينة. الـ TRUNCATE بتفضي الجدول كله بسرعة. الـ DROP بتمسح الجدول وهيكله بالكامل.})$

## 5\. Data Querying (DQL)

### The `SELECT` Statement

The fundamental command for retrieving data.

$(\text{ده أهم أمر وهو اللي بيطلعلك البيانات اللي عايزها من الداتابيز.})$

```sql
-- Retrieve all columns and all rows from the Employees table
SELECT * FROM Employees;
```

### `DISTINCT` and `FETCH`

  * **`DISTINCT`**: Eliminates duplicate rows from the result set. $(\text{بيصفي النتايج وبيجيب القيم الفريدة فقط.})$
  * **`FETCH`**: Limits the number of rows returned by a query (often used with `ORDER BY`). $(\text{بيحدد عدد الصفوف اللي ترجعلك في النتيجة، مفيد عشان تجيب 'أول 10' مثلاً.})$

<!-- end list -->

```sql
-- Get unique department IDs
SELECT DISTINCT dept_id FROM Employees;

-- Get the top 10 most highly paid employees (Oracle 12c+ syntax)
SELECT employee_id, salary
FROM Employees
ORDER BY salary DESC
FETCH FIRST 10 ROWS ONLY;
```

### The `WHERE` Clause

Filters records based on a specified condition.

$(\text{شرط التصفية، بيخليك تجيب الصفوف اللي مطابقة لشرط معين بس.})$

```sql
-- Find employees with a salary greater than 50000
SELECT last_name, salary
FROM Employees
WHERE salary > 50000;
```

### Operators

Used within the `WHERE` clause to form conditions:

| Type | Operator | Description | Example |
| :--- | :--- | :--- | :--- |
| **Comparison** | `=`, `!=` (`<>`), `>`, `<`, `>=`, `<=` | Test equality/inequality/magnitude. | `WHERE salary = 60000` |
| **Logical** | `AND`, `OR`, `NOT` | Combine multiple conditions. | `WHERE dept_id = 50 AND salary > 50000` |

### Aggregate Functions

Perform a calculation on a set of rows and return a single summary value.

$(\text{دوال التجميع، بتعمل عملية حسابية على مجموعة من الصفوف وتطلع ناتج واحد ملخص ليها، زي المتوسط أو المجموع.})$

| Function | Description | Example |
| :--- | :--- | :--- |
| **`COUNT()`** | Number of rows. | `COUNT(*)` |
| **`SUM()`** | Sum of values. | `SUM(salary)` |
| **`AVG()`** | Average of values. | `AVG(salary)` |

```sql
-- Get the average salary across the company
SELECT AVG(salary) AS avg_salary FROM Employees;
```

### `GROUP BY` and `ORDER BY`

  * **`GROUP BY`**: Groups rows that have the same values in specified columns into summary rows. $(\text{بتجمع الصفوف المتشابهة في مجموعة عشان تطبق عليها دوال التجميع.})$
  * **`ORDER BY`**: Sorts the result set by one or more columns. $(\text{بتنظم النتايج يا تصاعدي } (\text{ASC}) \text{ يا تنازلي } (\text{DESC}).)$

<!-- end list -->

```sql
-- Calculate the total salary for each department, sorted by total salary
SELECT dept_id, SUM(salary) AS total_dept_salary
FROM Employees
GROUP BY dept_id
ORDER BY total_dept_salary DESC;
```

### `HAVING` and its Difference with `WHERE`

  * **`HAVING`**: Filters groups created by the `GROUP BY` clause. $(\text{بتفلتر المجموعات اللي عملها } \text{GROUP BY} \text{، ودي لازم تستخدم فيها دالة تجميع.})$
  * **`WHERE`**: Filters individual rows *before* they are grouped. $(\text{بتفلتر الصفوف قبل ما تتجمع.})$

<!-- end list -->

```sql
-- Find departments where the total salary expense is over 500,000
SELECT dept_id, SUM(salary) AS total_dept_salary
FROM Employees
GROUP BY dept_id
HAVING SUM(salary) > 500000;
```

| Feature | `WHERE` Clause | `HAVING` Clause |
| :--- | :--- | :--- |
| **Execution** | Executes **before** `GROUP BY`. | Executes **after** `GROUP BY`. |
| **Applicability**| Filters individual **rows**. | Filters aggregated **groups**. |

### `LIKE`, `IN`, `BETWEEN`

| Operator | Description | Example |
| :--- | :--- | :--- |
| **`LIKE`** | Used for pattern matching. $(\text{بتبحث عن نص معين فيه جزء من القيمة، بنستخدم } \text{%} \text{ لو عايز أي عدد من الحروف و } \text{_} \text{ لحرف واحد.})$ | `WHERE last_name LIKE 'Smi%'` |
| **`IN`** | Used to specify multiple possible values for a column. $(\text{بتجيب الصفوف اللي قيمة العمود فيها مطابقة لأي قيمة من القائمة اللي أنت بتحددها.})$ | `WHERE dept_id IN (10, 20, 30)` |
| **`BETWEEN`** | Used to select values within a given range (inclusive). $(\text{بتجيب القيم اللي بين رقمين محددين، شاملة الرقمين نفسهم.})$ | `WHERE salary BETWEEN 50000 AND 75000` |

### Column and Table Aliases

Aliases are temporary names given to a table or a column to make the query easier to read and manage.

$(\text{اسم مؤقت للعمود أو الجدول عشان نختصر أو نخلي اسم العمود في النتيجة أوضح.})$

```sql
-- Column Alias
SELECT employee_id AS ID, last_name "Employee Name"
FROM Employees;

-- Table Alias
SELECT e.last_name, d.dept_name
FROM Employees e, Departments d
WHERE e.dept_id = d.dept_id;
```

### The `CASE` Expression

A powerful tool for performing conditional logic (IF/THEN/ELSE) directly within a query.

$(\text{بتعمل شرط جوه جملة الـ SELECT نفسها، بتقول: لو الشرط ده اتحقق، طلع القيمة دي، وإلا طلع القيمة دي.})$

```sql
SELECT
    last_name,
    CASE
        WHEN salary < 50000 THEN 'Low'
        ELSE 'High'
    END AS Salary_Level
FROM Employees;
```

## 6\. Joining Multiple Tables

Joins combine rows from two or more tables based on a related column between them.

$(\text{الـ Joins هي اللي بتجمع البيانات من جدولين أو أكتر عشان تجيب معلومة كاملة.})$

### Inner Join

Returns only the rows that have matching values in **both** tables.

$(\text{بتجيب الصفوف اللي ليها ماتش } (\text{قيمة مطابقة}) \text{ في الجدولين بس.})$

```sql
SELECT e.last_name, d.dept_name
FROM Employees e
INNER JOIN Departments d ON e.dept_id = d.dept_id;
```

### Full Outer Join

Returns all rows from **both** tables, with `NULL` values where there is no match in the other table.

$(\text{بتجيب كل الصفوف من الجدولين، ولو مفيش ماتش بتحط } \text{NULL} \text{ في البيانات الناقصة.})$

```sql
SELECT e.last_name, d.dept_name
FROM Employees e
FULL OUTER JOIN Departments d ON e.dept_id = d.dept_id;
```

### Left and Right Outer Join

  * **Left Join**: Returns all rows from the **left** table and the matched rows from the right table. $(\text{بتجيب كل بيانات الجدول الشمال } (\text{Left}) \text{ والصفوف اللي ليها ماتش من الجدول اليمين.})$
  * **Right Join**: Returns all rows from the **right** table and the matched rows from the left table. $(\text{العكس، بتجيب كل بيانات الجدول اليمين.})$

<!-- end list -->

```sql
-- Left Join
SELECT e.last_name, d.dept_name
FROM Employees e
LEFT JOIN Departments d ON e.dept_id = d.dept_id;
```

### Self Join

A join of a table to itself. This is often used when a table has a foreign key that references its own primary key.

$(\text{بتوصل الجدول بنفسه، زي لما تكون عايز تعرف مين هو مدير كل موظف، والمديرين والموظفين كلهم في نفس الجدول.})$

```sql
-- Find the name of each employee's manager
SELECT worker.last_name AS Employee, manager.last_name AS Manager
FROM Employees worker
JOIN Employees manager ON worker.manager_id = manager.employee_id;
```

## 7\. Nested Queries (Subqueries)

A subquery is a query nested inside another query. They are used to return data that will be used by the outer query.

$(\text{استعلام جوه استعلام تاني. يعني الاستعلام الداخلي بيطلع نتيجة، والاستعلام الخارجي بيستخدم النتيجة دي عشان يكمل شغله.})$

```sql
-- Find employees whose salary is greater than the average salary of all employees
SELECT last_name, salary
FROM Employees
WHERE salary > (
    SELECT AVG(salary) FROM Employees
);
```

## 8\. Performance and Structure Tools

### Indexes

Indexes are special lookup tables that the database search engine can use to speed up data retrieval.

$(\text{زي فِهرس الكتاب بالظبط، بيخلي الداتابيز تلاقي البيانات اللي بتدور عليها بسرعة رهيبة بدل ما تدور صف صف.})$

```sql
-- Create an index on the last_name column
CREATE INDEX idx_emp_lastname
ON Employees (last_name);
```

### Views

A view is a stored query that acts like a virtual table. It doesn't store data itself but displays data from the underlying tables.

$(\text{جدول وهمي مبني على استعلام. مفيد عشان تخفي أعمدة معينة لأسباب أمنية، أو عشان تبسّط استعلام معقد بدل ما تكتبه كل مرة.})$

```sql
-- Create a view that only shows employee names and their department names
CREATE VIEW Employee_Department_View AS
SELECT e.last_name, d.dept_name
FROM Employees e
JOIN Departments d ON e.dept_id = d.dept_id;

-- You can query the view just like a table
SELECT * FROM Employee_Department_View;
```
