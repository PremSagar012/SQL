BASICS

WHERE:
Used to FILTER the data in the output
Always after FROM

Syntax:
SELECT column_name1, column_name2 FROM table_name WHERE condition

Example:
SELECT * FROM payment WHERE amount = 10.99
SELECT first_name, last_name FROM customer WHERE first_name = 'ADAM'

WHERE Operators:
We can use operators like >, <, =, !=, is null, is not null

Example:
SELECT COUNT(*) FROM rental WHERE amount >=20

AND / OR :
Used to connect two conditions

Syntax:
SELECT column_name1, column_name2 FROM table_name WHERE conditional AND condition2 AND condition3

Example:
SELECT * FROM payment WHERE amount = 10.99 OR amount = 9.99

*BETWEEN:
Used to filer a range of values

Syntax:
SELECT payment_id, payment_date 
FROM payment
WHERE amount BETWEEN 1.99 AND 3.5

SELECT payment_id, payment_date 
FROM payment
WHERE amount NOT BETWEEN 1.99 AND 3.5

IN:
Used to include more than one condition

Example:
SELECT * FROM customer
WHERE customer_id IN (1,3,6,8)

SELECT * FROM customer
WHERE customer_id IN ('PREM', 'SIMBA', 'HONEY')

LIKE:
Used to filer by matching against a pattern
Use wildcards: _ any single character 
Use wildcards: % any sequence of  characters

Example:
SELECT * FROM actor WHERE first_name LIKE 'A%'

Commenting:
COmment to make code more readable and understandable
Use -- Single line comment
Use /*.....*/ Multiple line comment