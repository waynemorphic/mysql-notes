## SQL PROBLEMS WITH SOLUTIONS

### 1. Query a list of CITY names from STATION for cities that have an even ID number. Print the results in any order, but exclude duplicates from the answer.

`SELECT DISTINCT CITY FROM STATION WHERE ID % 2 = 0;`

### 2. Find the difference between the total number of CITY entries in the table and the number of distinct CITY entries in the table.

`SELECT COUNT(CITY) - COUNT(DISTINCT CITY) FROM STATION;`

### 3. Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.

`SELECT CITY LENGTH(CITY) AS lengthofcity FROM STATION ORDER BY lengthofcity CITY LIMIT 1; `

`SELECT CITY LENGTH(CITY) AS lengthofcity FROM STATION ORDER BY lengthofcity DESC CITY LIMIT 1; `

### 4. Query the list of CITY names starting with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates.

`SELECT DISTINCT CITY FROM STATION WHERE CITY LIKE 'A%' OR CITY LIKE 'E%' OR CITY LIKE 'I%' OR CITY LIKE 'O%' OR CITY LIKE 'U%';`

### 5. Query the list of CITY names ending with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates.

*Solution 1:* `SELECTT DISTINCT CITY FROM STATION WHERE CITY REGEXP '[aeiou]$';`

*Solution 2:* `SELECT DISTINCT CITY FROM STATION WHERE CITY LIKE '%a' OR CITY LIKE '%e' OR CITY LIKE '%i' OR CITY LIKE '%o' OR CITY LIKE '%u';`

*Solution 3:* 

`SELECT DISTINCT CITY FROM STATION WHERE CITY LIKE '%a';`

`SELECT DISTINCT CITY FROM STATION WHERE CITY LIKE '%e';`

`SELECT DISTINCT CITY FROM STATION WHERE CITY LIKE '%i';`

`SELECT DISTINCT CITY FROM STATION WHERE CITY LIKE '%o';`

`SELECT DISTINCT CITY FROM STATION WHERE CITY LIKE '%u';`