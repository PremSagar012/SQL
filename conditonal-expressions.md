📘 SQL Functions and Operators Reference
This document provides a quick reference to commonly used SQL mathematical functions, conditional expressions, and type conversion utilities.

🔢 Mathematical Operators
Operator	Description
+	Addition
-	Subtraction
*	Multiplication
/	Division
%	Modulo (remainder)
^	Exponentiation (power)

🧮 Mathematical Functions
Function	Description	Example
abs(x)	Returns the absolute value of x	abs(-7) → 7
round(x, d)	Rounds x to d decimal places	round(3.14159, 2) → 3.14
ceiling(x) / ceil(x)	Rounds x up to the nearest integer	ceiling(4.2) → 5
floor(x)	Rounds x down to the nearest integer	floor(4.9) → 4

🧠 Conditional Logic
CASE WHEN
Acts like an IF/THEN statement by checking conditions in order and returning the corresponding result.

Syntax:

sql
Copy
Edit
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    ...
    WHEN conditionN THEN resultN
    ELSE result
END
Example:

sql
Copy
Edit
CASE
    WHEN score >= 90 THEN 'A'
    WHEN score >= 80 THEN 'B'
    ELSE 'F'
END
🚫 COALESCE
Returns the first non-NULL value from a list of arguments.

Syntax:

sql
Copy
Edit
COALESCE(value1, value2, ..., default_value)
Example:

sql
Copy
Edit
COALESCE(NULL, NULL, 'default') → 'default'
🔄 CAST
Converts a value from one data type to another.

Syntax:

sql
Copy
Edit
CAST(value AS data_type)
Example:

sql
Copy
Edit
CAST(salary AS INTEGER)
✂️ REPLACE
Replaces occurrences of a substring within a string with another substring.

Syntax:

sql
Copy
Edit
REPLACE(column, 'old_text', 'new_text')
Example:

sql
Copy
Edit
REPLACE(flight_no, 'PG', 'FL') → 'FL123'