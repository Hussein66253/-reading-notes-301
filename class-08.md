# SQL
 ## What is SQL and how does it work?
 - In *database systems*, **SQL( Structured Query Language)** statements are used to generate **queries** from a client program to the database, this can allow the users to execute a wide range of **fast** data *manipulation*, so SQL is the ***main language*** that allows our database servers to **store** and **edit** the data on it.

        - There are many popular SQL databases including SQLite, MySQL, Postgres, Oracle and Microsoft SQL Server. All of them support the common SQL language standard, which is what this site will be teaching, but each implementation can differ in the additional features and storage types it supports.

### SELECT queries
- to Select query for a specific column 

        SELECT column FROM mytable;
- to Select query for a specific columns 

        SELECT column, another_column, …
        FROM mytable;
- to Select query for all columns

        SELECT * FROM mytable;
-  to Select query with constraints

        SELECT column, another_column, …
        FROM mytable
        WHERE condition
            AND/OR another_condition
            AND/OR …;