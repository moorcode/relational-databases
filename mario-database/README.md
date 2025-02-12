# Relational Databases

## Mario Database

> [!NOTE]
> In this 165-lesson course, you will learn the basics of a relational database by creating a PostgreSQL database filled with video game characters.
>
>This course runs in a virtual Linux machine using Gitpod. Start the course at [freeCodeCamp](https://www.freecodecamp.org/learn/relational-database/learn-relational-databases-by-building-a-mario-database/build-a-mario-database).
>
> __Checkpoints:__ 
> \l, CREATE, \c, \db, \d, ALTER, ADD, DROP

1. The first thing you need to do is start the terminal. Do that by clicking the _hamburger_ menu at the top left of the screen, going to the "terminal" section, and clicking _new terminal_. Once you open a new one, type `echo hello PostgreSQL` into the terminal and press enter.

2. Your virtual machine comes with PostgreSQL installed. You will use the Psql terminal application to interact with it. Log in by typing `psql --username=freecodecamp --dbname=postgres` into the terminal and pressing enter.

```bash 
camper: /project$ psql --username=freecodecamp --dbname=postgres
Border style is 2.
Title is " ".
Pager usage is off.
psql (12.17 (Ubuntu 12.17-1.pgdg22.04+1))
SSL connection (protocol: TLSv1.3, cipher: TLS_AES_256_GCM_SHA384, bits: 256, compression: off)
Type "help" for help.

postgres=> 
```

3. Notice that the prompt changed to let you know that you are now interacting with PostgreSQL. First thing to do is see what databases are here. Type `\l` into the prompt to __list__ them.

```bash
postgres=> \l
                               List of databases
+-----------+----------+----------+---------+---------+-----------------------+
|   Name    |  Owner   | Encoding | Collate |  Ctype  |   Access privileges   |
+-----------+----------+----------+---------+---------+-----------------------+
| postgres  | postgres | UTF8     | C.UTF-8 | C.UTF-8 |                       |
| template0 | postgres | UTF8     | C.UTF-8 | C.UTF-8 | =c/postgres          +|
|           |          |          |         |         | postgres=CTc/postgres |
| template1 | postgres | UTF8     | C.UTF-8 | C.UTF-8 | =c/postgres          +|
|           |          |          |         |         | postgres=CTc/postgres |
+-----------+----------+----------+---------+---------+-----------------------+
(3 rows)
postgres=> 
```

4. The databases you see are there by default. You can make your own with `CREATE DATABASE database_name;`. The capitalized words are keywords telling PostgreSQL what to do. The name of the database is the lowercase word. Note that all commands need a semi-colon at the end. __Create a database__ named `first_database`.

```bash
postgres=> CREATE DATABASE first_database;
CREATE DATABASE
postgres=> 
```

5. Use the list shortcut command again to make sure your new database is there.

6. It worked. Your new database is there. If you don't get a message after entering a command, it means it's incomplete and you likely forgot the semi-colon. You can just add it on the next line and press enter to finish the command. Create another database named `second_database`.

```bash
postgres=>                                     List of databases
+-----------------+--------------+----------+---------+---------+-----------------------+
|      Name       |    Owner     | Encoding | Collate |  Ctype  |   Access privileges   |
+-----------------+--------------+----------+---------+---------+-----------------------+
| first_database  | freecodecamp | UTF8     | C.UTF-8 | C.UTF-8 |                       |
| postgres        | postgres     | UTF8     | C.UTF-8 | C.UTF-8 |                       |
| second_database | freecodecamp | UTF8     | C.UTF-8 | C.UTF-8 |                       |
| template0       | postgres     | UTF8     | C.UTF-8 | C.UTF-8 | =c/postgres          +|
|                 |              |          |         |         | postgres=CTc/postgres |
| template1       | postgres     | UTF8     | C.UTF-8 | C.UTF-8 | =c/postgres          +|
|                 |              |          |         |         | postgres=CTc/postgres |
+-----------------+--------------+----------+---------+---------+-----------------------+
(5 rows)

```

7. You can __connect__ to a database by entering `\c database_name`. You need to __connect__ to add information. __Connect__ to your `second_database`.

```bash
postgres=> \c second_database 
SSL connection (protocol: TLSv1.3, cipher: TLS_AES_256_GCM_SHA384, bits: 256, compression: off)
You are now connected to database "second_database" as user "freecodecamp".
second_database=> 
```

8. You should see a message that you are connected. Notice that the prompt changed to `second_database=>`. So the `postgres=>` prompt before must have meant you were connected to that database. A database is made of tables that hold your data. Enter `\d` to __display__ the tables.

```bash
second_database=> \d
Did not find any relations.
second_database=> 
```

6. Looks like there're no tables or relations yet. Similar to how you created a database, you can __create a table__ with `CREATE TABLE table_name();`. Note that the parenthesis are needed for this one. It will create the table in the database you are connected to. Create a table named `first_table` in `second_database`.

```bash
second_database=> CREATE TABLE first_table();
CREATE TABLE
second_database=> 
```

7. View the tables in `second_database` again with the display command. You should see your new table there with a little meta data about it.

```bash
second_database=> \d
second_database=>                List of relations
+--------+-------------+-------+--------------+
| Schema |    Name     | Type  |    Owner     |
+--------+-------------+-------+--------------+
| public | first_table | table | freecodecamp |
+--------+-------------+-------+--------------+
(1 row)


second_database=> 
```

8. Create another new table in this database. Give it a name of `second_table`.

```bash
second_database=> CREATE TABLE second_table();
CREATE TABLE
second_database=> 
```

9. There should be two tables in this database now. Display them again to make sure.

```bash
second_database=> \d
second_database=>                List of relations
+--------+--------------+-------+--------------+
| Schema |     Name     | Type  |    Owner     |
+--------+--------------+-------+--------------+
| public | first_table  | table | freecodecamp |
| public | second_table | table | freecodecamp |
+--------+--------------+-------+--------------+
(2 rows)


second_database=> 
```

10. You can __view more details__ about a table by adding the table name after the __display__ command like this: `\d table_name`. View more details about your `second_table`.

```bash
second_database=> \d second_table 
second_database=>            Table "public.second_table"
+--------+------+-----------+----------+---------+
| Column | Type | Collation | Nullable | Default |
+--------+------+-----------+----------+---------+
+--------+------+-----------+----------+---------+


second_database=> 
```

11. Tables need __columns__ to describe the data in them, yours doesn't have any yet. Here's an example of how to add one: `ALTER TABLE table_name ADD COLUMN column_name DATATYPE;`. __Add a column__ to `second_table` named `first_column`. Give it a __data type__ of `INT`. `INT` stands for __integer__. Don't forget the semi-colon. 😄

```bash
second_database=> ALTER TABLE second_table ADD COLUMN first_column INT;
ALTER TABLE
second_database=> 
```

12. Looks like it worked. Display the details of `second_table` again to see if your new column is there.

```bash
second_database=> \d second_table
                Table "public.second_table"
+--------------+---------+-----------+----------+---------+
|    Column    |  Type   | Collation | Nullable | Default |
+--------------+---------+-----------+----------+---------+
| first_column | integer |           |          |         |
+--------------+---------+-----------+----------+---------+

second_database=> 
```

13. Your column is there 😄 Use `ALTER TABLE` and `ADD COLUMN` to add another column to `second_table` named `id` that's a type of `INT`.
> [!TIP]
> Press _up arrow_ to cycle through previous commands

```bash
second_database=> ALTER TABLE second_table ADD COLUMN id INT;
ALTER TABLE
second_database=>
```

14. Your table should have an `id` column added. View the details of `second_table` to make sure.

```bash
second_database=> \d second_table
second_database=>                 Table "public.second_table"
+--------------+---------+-----------+----------+---------+
|    Column    |  Type   | Collation | Nullable | Default |
+--------------+---------+-----------+----------+---------+
| first_column | integer |           |          |         |
| id           | integer |           |          |         |
+--------------+---------+-----------+----------+---------+


second_database=> 
```

15. Add another column to `second_table` named `age`. Give it a data type of `INT`.

```bash
second_database=> ALTER TABLE second_table ADD COLUMN age INT;
ALTER TABLE
second_database=> 
```

16. Take a look at the details of `second_table` again.

```bash
second_database=> \d second_table
                Table "public.second_table"
+--------------+---------+-----------+----------+---------+
|    Column    |  Type   | Collation | Nullable | Default |
+--------------+---------+-----------+----------+---------+
| first_column | integer |           |          |         |
| id           | integer |           |          |         |
| age          | integer |           |          |         |
+--------------+---------+-----------+----------+---------+

second_database=> 
```
-
17. Those are some good looking columns. You will probably need to know how to __remove__ them. Here's an example: `ALTER TABLE table_name DROP COLUMN column_name;`. __Drop__ your `age` column.

```bash
second_database=> ALTER TABLE second_table DROP COLUMN age;
ALTER TABLE
second_database=> 
```

18. View the details of `second_table` to see if it's gone.

```bash
second_database=> \d second_table
                Table "public.second_table"
+--------------+---------+-----------+----------+---------+
|    Column    |  Type   | Collation | Nullable | Default |
+--------------+---------+-----------+----------+---------+
| first_column | integer |           |          |         |
| id           | integer |           |          |         |
+--------------+---------+-----------+----------+---------+

second_database=> 
```

19. It's gone. Use the `ALTER TABLE` and `DROP COLUMN` keywords again to drop `first_column`.

```bash
second_database=> ALTER TABLE second_table DROP COLUMN first_column ;
ALTER TABLE
second_database=> 
```

20. A common data type is `VARCHAR`. It's a short string of characters. You need to give it a maximum length when using it like this: `VARCHAR(30)`.

Add a new column to `second_table`, give it a name of name and a data type of `VARCHAR(30)`.

```bash
second_database=> ALTER TABLE second_table ADD COLUMN name VARCHAR(30);
ALTER TABLE
second_database=> 
```

21. Take a look at the details of `second_table` to see your columns.

```bash
second_database=> \d second_table
second_database=>                     Table "public.second_table"
+--------+-----------------------+-----------+----------+---------+
| Column |         Type          | Collation | Nullable | Default |
+--------+-----------------------+-----------+----------+---------+
| id     | integer               |           |          |         |
| name   | character varying(30) |           |          |         |
+--------+-----------------------+-----------+----------+---------+


second_database=> 
```

22. You can see the `VARCHAR` type there. The `30` means the data in it can be a max of 30 characters. You named that column `name`, it should have been `username`. Here's how you can __rename__ a column: `ALTER TABLE table_name RENAME COLUMN column_name TO new_name;`. __Rename__ the `name` column to `username`.

```bash
second_database=> ALTER TABLE second_table RENAME COLUMN name TO username;
ALTER TABLE
second_database=> 
```

23. Take a look at the details of `second_table` again to see if it got renamed.

```bash
second_database=> \d second_table
                     Table "public.second_table"
+----------+-----------------------+-----------+----------+---------+
|  Column  |         Type          | Collation | Nullable | Default |
+----------+-----------------------+-----------+----------+---------+
| id       | integer               |           |          |         |
| username | character varying(30) |           |          |         |
+----------+-----------------------+-----------+----------+---------+

second_database=> 
```

24. It worked. __Rows__ are the actual data in the table. You can add one like this: `INSERT INTO table_name(column_1, column_2) VALUES(value1, value2);`. __Insert a row__ into `second_table`. Give it an `id` of `1`, and a `username` of `Samus`. The `username` column expects a `VARCHAR`, so you need to put Samus in single quotes like this: `'Samus'`.

```bash
second_database=> INSERT INTO second_table(id, username) VALUES (1, 'Samus');
INSERT 0 1
second_database=> 
```

25. 

```bash

```

26. 

```bash

```

27. 

```bash

```

28. 

```bash

```

29. 

```bash

```

30. 

```bash

```
