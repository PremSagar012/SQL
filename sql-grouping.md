This document provides a concise and professional reference to commonly used SQL aggregate, string, and date/time functions, along with syntax examples. It is suitable for learning, interviews, or quick lookup during development.

📊 Aggregate Functions
Aggregate functions perform calculations on multiple rows and return a single value.

Function	Description	Example
SUM()	Calculates the total sum	SELECT SUM(amount) FROM payment;
AVG()	Returns the average value	SELECT AVG(price) FROM products;
MIN()	Returns the smallest value	SELECT MIN(age) FROM customers;
MAX()	Returns the largest value	SELECT MAX(salary) FROM employees;
COUNT()	Returns the number of rows	SELECT COUNT(*) FROM orders;

🧮 Grouping & Filtering Aggregates
GROUP BY
Used to group rows that have the same values in specified columns for aggregation.

sql
Copy
Edit
SELECT category, COUNT(*) 
FROM products
GROUP BY category;
HAVING
Filters grouped records based on aggregate conditions.

sql
Copy
Edit
SELECT category, COUNT(*) 
FROM products
GROUP BY category
HAVING COUNT(*) > 10;
🔤 String Functions
Case Conversion
Function	Description	Example
UPPER()	Converts string to uppercase	SELECT UPPER(first_name) FROM users;
LOWER()	Converts string to lowercase	SELECT LOWER(email) FROM customers;

String Length
sql
Copy
Edit
SELECT LENGTH(name) FROM products;
Left & Right Substrings
Function	Description	Example
LEFT()	Extracts characters from the left	SELECT LEFT(name, 3) FROM employees;
RIGHT()	Extracts characters from the right	SELECT RIGHT(name, 2) FROM employees;

Nested LEFT and RIGHT Example
To get the second letter from the first_name:

sql
Copy
Edit
SELECT RIGHT(LEFT(first_name, 2), 1) 
FROM customers;
🔗 Concatenation
SQLite uses || to concatenate strings.

sql
Copy
Edit
SELECT 
  RIGHT(last_name, 1) || LEFT(first_name, 2) 
FROM 
  customers;
🔍 Position & Substring
POSITION
Returns the position of a character or substring in a string.

sql
Copy
Edit
SELECT POSITION('@' IN email) 
FROM customers;
SUBSTRING
Extracts a substring from a given string.

sql
Copy
Edit
SELECT SUBSTRING(email FROM 1 FOR 5) 
FROM customers;
📅 Date/Time Functions
EXTRACT
Extracts parts (e.g., year, month, day) from a date or timestamp.

sql
Copy
Edit
SELECT EXTRACT(YEAR FROM created_at) 
FROM orders;
TO_CHAR
Converts dates or numbers to formatted strings.

sql
Copy
Edit
-- Format a date as 'YYYY-MM-DD'
SELECT TO_CHAR(order_date, 'YYYY-MM-DD') 
FROM orders;

-- Format a number with 2 decimal places
SELECT TO_CHAR(price, 'FM999999.00') 
FROM products;