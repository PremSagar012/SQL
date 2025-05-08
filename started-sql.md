What is SQL?
Structured Query Language
It is the language used to interact with the database

WHat is Database?
Database is used to store data in the form of tables

What is Schema?
It is basically an additional layer helps to organize and structure the database

*SELECT:
Most basic statement SQL
Used to select and return data

Syntax:
SELECT column_name FROM tale_name

Example:
SELECT first_name FROM actor -> To select one column
SELECT first_name, last_name FROM actor -> To select two columns
SELECT * FROM actor -> To select all columns

*ORDER BY:
Used to order results based on a column
Alphabetically, numerically, chronologically (Date or Time) , etc

Syntax:
SELECT column_name1, column_name2 FROM tale_name ORDER BY column_name1

Example:
SELECT first_name, last_name FROM actor ORDER BY first_name -> Ascending order
SELECT first_name, last_name FROM actor ORDER BY first_name DESC -> Descending order
SELECT first_name, last_name FROM actor ORDER BY first_name DESC, last_name -> If same first names then it will order the last_name
DESC -> Descending
ASC -> Ascending

*We can use column number instead of names
Example:
SELECT first_name FROM actor
SELECT 1 FROM actor

*SELECT DISTINCT:
Used to select the distinct values in the table

Syntax:
SELECT DISTINCT column_name FROM tale_name 

*LIMIT:
Used to limit the number of rows in the output
Always at the end of our query

Syntax:
SELECT DISTINCT column_name FROM tale_name LIMIT n

Example:
SELECT first_name FROM actor LIMIT 4

COUNT (Function):
Used to count the number of rows in a output
Used often in combination with grouping and filtering
Nulls will not be counted

Syntax:
SELECT COUNT(column_name) FROM tale_name

Example:
SELECT COUNT(first_name) FROM actor
SELECT COUNT(DISTINCT first_name) FROM actor