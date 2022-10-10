# MYSQL NOTES AND SOLUTIONS TO ERRORS

## NOTES
### Create Database
`CREATE DATABASE <database name`;

### Show database
- To show the newly created database, run: `SHOW CREATE DATABASE <database name>`
- To show a list of databases, run: `SHOW DATABASES;`

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