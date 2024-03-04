# This is simple PostgreSQL Assignment

## FullStack | Assignment-7

1. What is PostgreSQL?

Ans: PostgreSQL is an open-source, Relational DataBase Management System(RDBMS). PostgreSQL is ACID(Atomicity, Consistency, Isolation, Durability) Compliance and Advanced SQL Supported DataBase Management System.

2. What is the purpose of a database schema in PostgreSQL?

Ans: In PostgreSQL or any DataBase Management System(DBMS) or Relational DataBase Management System(RDBMS), database schema serve several important purposes.

Some purposes are discussed below.

- A schema provides a structure for our data. This structure helps organize our database.

- A schema helps enforce data integrity rules. Data integrity rules like primary key, foreign key, unique, not null, etc.

- We can protect Schemas in PostgreSQL by specific user or user roles.

3. Explain the primary key and foreign key concepts.

Ans: Primary key is a unique identifier for each row in PostgreSQL. On the other hand, using a foreign key creates relationship between two tables. We can join two or multiple tables using a foreign key. One table's primary key can be another table's foreign key.

4. What is the difference between the VARCHAR and CHAR data types?

Ans: In PostgreSQL, both data types, VARCHAR and CHAR are character data types, used for storing strings.

The CHAR data type use for fixed-length string. That means the CHAR data type store always same length string. If the inserted value is shorter than CHAR length, CHAR padding it with spaces to the specified length. If the inserted string is longer than the CHAR length, CHAR truncates the string to fit the specified length.

The VARCHAR data type is used for the defined max-length for the string. That means the VARCHAR allows a max level length of string. If the inserted value is shorter than VARCHAR length, than it's ok and no problem with this insertion and not padding it with spaces to the specified length.

5. Explain the purpose of the WHERE clause in a SELECT statement.

Ans: In PostgreSQL, where clause is used in select statement. Where is a clause for writing conditions for retrieving, updating, and deleting data from relations. On the other hand, select is the statement, It's used for data retrieval from relations.

6. What are the LIMIT and OFFSET clauses used for?

Ans: Basically in the PostGreSQL LIMIT and OFFSET clauses are used for pagination. The LIMIT clauses is used to restrict the number of data or rows retried from relations. On the other hand, OFFSET clauses are used to define the number of rows or data skipped before starting a return set of data or rows or specify the starting point.

7. How can you perform data modification using UPDATE statements?

Ans: In PostgreSQL, we use UPDATE statements for modify our existing data or rows.

Example:

```
UPDATE employees
    SET employee_name = Test
    WHERE employee_id = 3;
```

8. What is the significance of the JOIN operation, and how does it work in PostgreSQL?

Ans: In PostgreSQL the JOIN operation is significant for combining or joining rows from two or more relations base on related column or foreign key. It allows to get data from multiple relations.

Example:

```
SELECT employee_name FROM employees
    JOIN departments USING(department_id);
```

9. Explain the GROUP BY clause and its role in aggregation operations.

Ans: In PostgreSQL GROUP BY clause use for perform aggregation operations or grouping data base on condition. GROUP BY clause creates a group of rows that have the same values.

Example:

```
SELECT department_name, avg(salary) FROM employees
    JOIN departments USING(department_id)
    GROUP BY department_name;
```

Some Aggregate Functions: SUM, AVG, COUNT, MIM, MAX.

10. What is the purpose of an index in PostgreSQL, and how does it optimize query performance?

Ans:
In PostgreSQL index is a database indexing used to speed up the retrieval of data or rows from a relations. For using indexing we need to CREATE INDEX into the database.

Example:

```
CREATE INDEX idx_employee_name ON employees(employee_name);
```
