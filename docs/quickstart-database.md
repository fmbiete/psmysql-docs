# Create a database and table

To create a database and table, use the `CREATE DATABASE` statement. You can optionally specify the character set and collation for the database in the statement. After the database is created, select the database using the `USE` statement or the `-D` option in the MySQL client. 

Create a table using the `CREATE TABLE` statement. You can specify the values for each column or use the DEFAULT keyword for columns with default values, data types, constraints, indexes, and other options. 

Insert data into the table using the `INSERT` statement. 

??? Example "Benefits and what to watch out for"

    Creating a database and table has the following benefits:

    - Store and organize your data in a structured and consistent way.
    - Query and manipulate your data using SQL.
    - Enforce data integrity and security using constraints, triggers, views, roles, and permissions.
    - Optimize your data access and performance using indexes, partitions, caching, and other techniques.

    When you create a table, design your database schema carefully, as changing it later may be difficult and costly. You should experiment with concurrency, transactions, locking, isolation, and other issues that may arise when multiple users access the same data. You must backup and restore your data regularly, as data loss or corruption may occur due to hardware failures, human errors, or malicious attacks.

## What to do


```{.bash data-prompt="mysql>"}
mysql> CREATE DATABASE mydb;
```

```{.bash data-prompt="mysql>"}
mysql> use mydb;
```

??? example "Expected output"

    ```{.text .no-copy}
    Database changed
    ```

## Create a table

Create a table in the database.

```{.bash data-prompt="mysql>"}
CREATE TABLE `employees` (
  `id` mediumint(8) unsigned NOT NULL auto_increment,
  `name` varchar(255) default NULL,
  `email` varchar(255) default NULL,
  `country` varchar(100) default NULL,
  PRIMARY KEY (`id`)
) AUTO_INCREMENT=1;
```

## INSERT INTO query

```{.bash data-prompt="mysql>"}
INSERT INTO `employees` (`name`,`email`,`country`)
VALUES
  ("Erasmus Richardson","posuere.cubilia.curae@outlook.net","England"),
  ("Jenna French","rhoncus.donec@hotmail.couk","Canada"),
  ("Alfred Dejesus","interdum@aol.org","Austria"),
  ("Hamilton Puckett","dapibus.quam@outlook.com","Canada"),
  ("Michal Brzezinski","magna@icloud.pl","Poland"),
  ("Zofia Lis","zofial00@hotmail.pl","Poland"),
  ("Aisha Yakubu","ayakubu80@outlook.com","Nigeria"),
  ("Miguel Cardenas","euismod@yahoo.com","Peru"),
  ("Luke Jansen","nibh@hotmail.edu","Netherlands"),
  ("Roger Pettersen","nunc@protonmail.no","Norway");
```

## Next steps

[Run SQL queries :material-arrow-right:](quickstart-queries.md){.md-button}