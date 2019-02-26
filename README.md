# SQL Notes

The queries to deal with relational database can be categories as:

- Data Definition Language: It is used to define the structure of the database. e.g; CREATE TABLE, ADD COLUMN, DROP COLUMN and so on.

- Data Manipulation Language: It is used to manipulate data in the relations. e.g.; INSERT, DELETE, UPDATE and so on.

- Data Query Language: It is used to extract the data from the relations. e.g.; SELECT

## Data Query Language

```sql
SELECT [DISTINCT] Attribute_List FROM R1,R2….RM
[WHERE condition]
[GROUP BY (Attributes)[HAVING condition]]
[ORDER BY(Attributes)[DESC]];
```

### AGGRATION FUNCTIONS

All aggregation functions return only 1 row.

- COUNT: Count function is used to count the number of rows in a relation
- SUM: SUM function is used to add the values of an attribute in a relation.
  ```sql
  SELECT SUM (AGE) FROM STUDENT;
  ```
- MIN, MAX, AVG

### GROUP BY

It is always combined with aggregation function which is computed on group.

```sql
SELECT ADDRESS, SUM(AGE) FROM STUDENT
GROUP BY (ADDRESS);
```

NOTE: An attribute which is not a part of GROUP BY clause can’t be used for selection. Any attribute which is part of GROUP BY CLAUSE can be used for selection but it is not mandatory.

This will result in error:

```sql
SELECT ROLL_NO, ADDRESS, SUM(AGE) FROM STUDENT
GROUP BY (ADDRESS);
```

## Most Important Commands

SELECT - extracts data from a database
UPDATE - updates data in a database
DELETE - deletes data from a database
INSERT INTO - inserts new data into a database
CREATE DATABASE - creates a new database
ALTER DATABASE - modifies a database
CREATE TABLE - creates a new table
ALTER TABLE - modifies a table
DROP TABLE - deletes a table
CREATE INDEX - creates an index (search key)
DROP INDEX - deletes an index
