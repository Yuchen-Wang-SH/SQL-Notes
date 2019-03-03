# SQL

## What can it do?

- SQL can execute queries against a database
- SQL can retrieve data from a database
- SQL can insert records in a database
- SQL can update records in a database
- SQL can delete records from a database
- SQL can create new databases
- SQL can create new tables in a database
- SQL can create stored procedures in a database
- SQL can create views in a database
- SQL can set permissions on tables, procedures, and views

## Most important commands

- SELECT - extracts data from a database
- UPDATE - updates data in a database
- DELETE - deletes data from a database
- INSERT INTO - inserts new data into a database
- CREATE DATABASE - creates a new database
- ALTER DATABASE - modifies a database
- CREATE TABLE - creates a new table
- ALTER TABLE - modifies a table
- DROP TABLE - deletes a table
- CREATE INDEX - creates an index (search key)
- DROP INDEX - deletes an index

## SELECT

### DISTINCT

```sql
SELECT COUNT(DISTINCT Country) FROM Customers;
```

### WHERE

```sql
SELECT * FROM Customers
WHERE Country='Mexico';
```

SQL requires single quotes around text values (most database systems will also allow double quotes).

#### Operators

Operator Description
= Equal

**<>** Not equal. Note: In some versions of SQL this operator may be written as !=

**BETWEEN** Between a certain range

- ```sql
  SELECT column_name(s)
  FROM table_name
  WHERE column_name BETWEEN value1 AND value2;
  ```

**LIKE** Search for a pattern

- % - The percent sign represents zero, one, or multiple characters
- \_ - The underscore represents a single character
- (And more [wildcards](https://www.w3schools.com/sql/sql_wildcards.asp).)
  ```sql
  SELECT * FROM Customers
  WHERE CustomerName LIKE '%a';
  ```

**IN** To specify multiple possible values for a column

- ```sql
  SELECT column_name(s)
  FROM table_name
  WHERE column_name IN (value1, value2, ...);
  ```
- ```sql
  SELECT column_name(s)
  FROM table_name
  WHERE column_name IN (SELECT STATEMENT);
  ```

**IS NULL and IS NOT NULL** Not possible to test for NULL values with comparison operators, such as =, <, or <>.

```sql
SELECT * FROM Customers
WHERE Country='Germany' AND (City='Berlin' OR City='München');
```

### ORDER BY

```sql
SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;
```

### LIMIT

```sql
-- MySQL
SELECT column_name(s)
FROM table_name
WHERE condition
LIMIT number;
```

### Alias

https://www.w3schools.com/sql/sql_alias.asp

## INSERT INTO

```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

Or

```sql
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```

## UPDATE

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

## DELETE

```sql
DELETE FROM table_name WHERE condition;
```
