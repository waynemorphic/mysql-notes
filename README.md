# MYSQL NOTES AND SOLUTIONS TO ERRORS

## NOTES
### Create Database
`CREATE DATABASE <database name`;

### Show database
- To show the newly created database, run: `SHOW CREATE DATABASE <database name>`
- To show a list of databases, run: `SHOW DATABASES;`

### Connect database
- `USE <database name>`

### Create table;
- `CREATE TABLE <table name>(<column name | data type>` <br> ie CREATE TABLE test(employee_id int, employee_name varchar(250);)

### List all tables in the database connected;
- `SHOW TABLES;`

### List details of a particular table
- `DESCRIBE <table name>;`

### Adding values into an empty table
- `INSERT INTO <table name>(<column name_1, column name_2, ... column name_n>) VALUES ();`
- For values, if value is of data type varchar, use `" "` and of type int, no need for string quotes

### Change values in a table
- `UPDATE <table name> SET <column name_1 = new value, column name_2 = new value> WHERE <specific value of a column in table>;`

### Show values of a specific table
- `SELECT * FROM <table name>;`

### Add a column as the last entry in a table
- `ALTER TABLE <table name> ADD <new column name> <type>;`

### Add a column before another column
- `ALTER TABEL <table name> ADD <new column name> <type> AFTER <column name before the new column>;`

### Add a column as the first entry of non-empty table
- `ALTER TABLE <table name> ADD <new table name> <type> FIRST;`
- 
## PROBLEMS AND SOLUTIONS
1. `SyntaxError: Unexpected identifier`
- This error is caused by the MYSQL Shell being in the javascript mode by default.
- Check whether the shell shows `MYSQL JS >`<br>
Solution:
- Run `\sql` to switch to SQL mode
- Then run `\connect root@localhost:<port number>`
- Then enter password for the root user or other user specified during the installation of MYSQL
- The port number is optional
2. `ERROR: 1064 (42000): You have an error in your SQL syntax;`
- This is commonly a syntax error. Check if your syntax is okay by referring to MYSQL documentation.