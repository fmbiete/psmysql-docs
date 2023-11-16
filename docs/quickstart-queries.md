# Run SQL queries

structured query language (SQL) Data Manipulation Language (DML) queries are statements that manipulate the data in a database.

??? Information "Different types of queries"

    There are four basic DML queries in Percona Server for MySQL: SELECT, INSERT, UPDATE, and DELETE.

    - SELECT queries retrieve data from one or more tables based on specified criteria. They are the most common type of DML queries and can be used for various purposes, such as displaying, filtering, sorting, aggregating, or joining data. SELECT queries do not modify the data in the database but can affect the performance if the query involves large or complex datasets.

    - UPDATE queries modify existing data in a table. They are used to change or correct the information stored in the database. UPDATE queries can update one or more columns and rows simultaneously, depending on the specified conditions. They may also fail if they violate any constraints or rules defined on the table.

    - INSERT queries add new data to a table. They are used to populate or expand the database with new information. INSERT queries can insert one or more rows at a time, depending on the syntax. They may fail if they violate any constraints or rules defined on the table, such as primary keys, foreign keys, unique indexes, or triggers.

    - DELETE queries remove existing data from a table. They are used to delete or clean up information no longer needed or relevant in the database. DELETE queries can delete one or more rows at a time, depending on the conditions specified. They may also trigger cascading deletes on related tables if foreign key constraints are enforced.

    Different queries are used for various purposes depending on the data manipulation or retrieval needs.

### SELECT query

```{.bash data-prompt="mysql>"}
mysql>SELECT id, name, email, country FROM employees WHERE country = 'Poland';
```

??? example "Expected output"

    ```{.text .no-copy}
    +----+-------------------+---------------------+---------+
    | id | name              | email               | country |
    +----+-------------------+---------------------+---------+
    |  5 | Michal Brzezinski | magnus@iclound.pl   | Poland  |
    |  6 | Zofia Lis         | zofial00@hotmail.pl | Poland  |
    +----+-------------------+---------------------+---------+
    ```

### UPDATE query

```{.bash data-prompt="mysql>"}
mysql> UPDATE employees SET name = 'Zofia Niemec' WHERE id = 6;
```

??? example "Expected output"

    ```{.text .no-copy}
    Query OK, 1 row affected (0.01 sec)
    Rows matched: 1  Changed: 1  Warnings: 0
    ```

Run a [Select](#select-query) with a WHERE clause to verify the update.

```{.bash data-prompt="mysql>"}
mysql> SELECT id, name, email, country FROM employees WHERE country = 'Poland';
```

??? example "Expected output"

    ```{.text .no-copy}
    +----+-------------------+---------------------+---------+
    | id | name              | email               | country |
    +----+-------------------+---------------------+---------+
    |  5 | Michal Brzezinski | magnus@iclound.pl   | Poland  |
    |  6 | Zofia Niemec      | zofial00@hotmail.pl | Poland  |
    +----+-------------------+---------------------+---------+
    2 rows in set (0.00 sec)
    ```

### INSERT query

Insert a row.

INSERT INTO `employees` (`name`,`email`,`country`)
VALUES
  ("Kenzo Sasaki","KenSasaki@outlook.com","Japan");

### DELETE query

Delete a row.

```{.bash data-prompt="mysql>"}
mysql> DELETE FROM employees WHERE id >= 11;
```

??? example "Expected output"

    ```{.text .no-copy}
    Query OK, 1 row affected (0.02 sec)
    ```

Run a [Select](#select-query) with a WHERE clause to verify the update.

```{.bash data-prompt="mysql>"}
mysql> SELECT id, name, email, country FROM employees WHERE id = 11;
```

## Next steps

[Clean up :material-arrow-right:](quickstart-exit.md){.md-button}