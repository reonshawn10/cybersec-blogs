+++ 
date = '2025-10-26' 
draft = false 
title = 'Weekly Cybersecurity Blog' 
+++

# Week 2 - SQL Basics for Cybersecurity (My Learning Log)

This week, I dived into SQL and explored how relational databases work. It's fascinating to see how tables can connect and communicate with each other using just a few commands.

---

## Basic Example - Creating and Working with a Table

### 1 - After creating the table (empty)

| student\_id | name | age |
| ----------- | ---- | --- |
| *(empty)*   |      |     |

### 2 - After inserting first entry

```sql
INSERT INTO student VALUES (1, 'shawn', 19);
```

| student\_id | name  | age |
| ----------- | ----- | --- |
| 1           | shawn | 19  |

### 3ï- After inserting multiple entries

```sql
INSERT INTO student VALUES
(2, 'alice', 20),
(3, 'bob', 21),
(4, 'charlie', 22);
```

| student\_id | name    | age |
| ----------- | ------- | --- |
| 1           | shawn   | 19  |
| 2           | alice   | 20  |
| 3           | bob     | 21  |
| 4           | charlie | 22  |

### 4ï- After updating a row

```sql
UPDATE student
SET name = 'rodrigues'
WHERE student_id = 1;
```

| student\_id | name      | age |
| ----------- | --------- | --- |
| 1           | rodrigues | 19  |
| 2           | alice     | 20  |
| 3           | bob       | 21  |
| 4           | charlie   | 22  |

### 5ï- After deleting a row

```sql
DELETE FROM student
WHERE student_id = 2;
```

| student\_id | name      | age |
| ----------- | --------- | --- |
| 1           | rodrigues | 19  |
| 3           | bob       | 21  |
| 4           | charlie   | 22  |

### 6ï- Final table before dropping

| student\_id | name      | age |
| ----------- | --------- | --- |
| 1           | rodrigues | 19  |
| 3           | bob       | 21  |
| 4           | charlie   | 22  |

### Adding a Foreign Key

```sql
ALTER TABLE orders
ADD CONSTRAINT fk_customer
FOREIGN KEY (customer_id)
REFERENCES customers(customer_id)
ON DELETE SET NULL;
```

---

## Core Concepts & Keywords (Recap)

- **Relational database:** A structured collection of tables that are connected.
- **Primary key:** Uniquely identifies each row.
- **Foreign key:** Connects tables and can have repeated or null values.
- **Composite key:** A primary key using multiple columns.

**Keywords:** `SELECT`, `FROM`, `ORDER BY`, `LIMIT`, `WHERE`

**Filtering:** Selecting rows based on conditions.

**Operators:** `=`, `<`, `>`, `<>`, `<=`, `>=`, `AND`, `OR`, `NOT`

**LIKE:** Used for pattern matching, often with `%`.

```sql
WHERE country LIKE 'US%'; -- matches US, USA, etc.
```

| country |
| ------- |
| US      |
| USA     |
| US123   |

### SELECT with ORDER BY and LIMIT example

```sql
SELECT *
FROM student
ORDER BY student_id DESC
LIMIT 2;
```

| student\_id | name    | age |
| ----------- | ------- | --- |
| 4           | charlie | 22  |
| 3           | bob     | 21  |

---

## Reflection

Working with SQL this week was really engaging. I learned not just the commands, but also how tables relate to each other, which makes databases feel alive. Practicing CREATE, INSERT, UPDATE, DELETE, and foreign key relationships helped me see how data integrity is maintained and why SQL is such a powerful tool.

