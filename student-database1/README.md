# Relational Databases

## Student Database 1

In this 140-lesson course, you will create a Bash script that uses SQL to enter information about your computer science students into PostgreSQL.

This course runs in a virtual Linux machine using Gitpod. Alternatively, download Postgres and Microsoft VS Code with these extensions: PostgreSQL by Microsoft, Rainbow CSV.

1. The first thing you need to do is start the terminal. Do that by clicking the "hamburger" menu at the top left of the screen, going to the "terminal" section, and clicking "new terminal". Once you open a new one, type `echo hello SQL` into the terminal and press enter.

2. On Gitpod, you are started with two `.csv` files with info about your computer science students. You should take a look at them. The top row in each file has titles, and the rest are values for those titles. You will be adding all that info to a PostgreSQL database. Log into the psql interactive terminal with `psql --username=postgres --dbname=postgres` to get started. Locally, you'll be asked for a password.

```

postgres=#

```

3. View the existing databases with the `\l` shortcut command to see what's here.

```

postgres=# \l


   Name    |  Owner   | Encoding | Locale Provider |          Collate           |           Ctype            | Locale | ICU Rules |   Access privileges
-----------+----------+----------+-----------------+----------------------------+----------------------------+--------+-----------+-----------------------
 postgres  | postgres | UTF8     | libc            | English_United States.1252 | English_United States.1252 |        |           |
 template0 | postgres | UTF8     | libc            | English_United States.1252 | English_United States.1252 |        |           | =c/postgres          +
-----------+----------+----------+-----------------+----------------------------+----------------------------+--------+-----------+--------------------
---
 postgres  | postgres | UTF8     | libc            | English_United States.1252 | English_United States.1252 |        |           |
 template0 | postgres | UTF8     | libc            | English_United States.1252 | English_United States.1252 |        |           | =c/postgres          +
           |          |          |                 |                            |                            |        |           | postgres=CTc/postgres
 template1 | postgres | UTF8     | libc            | English_United States.1252 | English_United States.1252 |        |           | =c/postgres          +
           |          |          |                 |                            |                            |        |           | postgres=CTc/postgres
(3 rows)

```

4.