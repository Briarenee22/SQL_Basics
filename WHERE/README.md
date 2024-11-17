# SQL NOTES: WHERE CLAUSE WITH LOGICAL OPERATORS 



## Overview 
The WHERE clause is used in SQL to filter results based on conditions. Logical operators refine these conditions to perform more complex queries.

`AND`: Returns rows when all conditions are true.
Example: Filtering for a specific year and month.

`OR`: Returns rows when any condition is true.
Example: Finding rows for either a specific year or month.

`NOT`: Negates a condition, returning rows where it's false.
Example: Excluding rows from a specific year.

`BETWEEN`: Filters rows within a range (inclusive).
Example: Selecting rows where values fall between 500 and 1000.

`LIKE`: Searches for patterns in string data with wildcards (% and _).
Example: Finding product names that start with 'Pro'.
     
## Example Queries and Explanations

Example 1: `AND` Operator:
```sql
SELECT*
FROM tutorial.aapl_historical__stock_price
WHERE year = 2014 AND month = 1; 

Explanation:
--* Links multiple conditions; returns where all conditions are TRUE


Example 2: Using `OR` Operator:
```sql
SELECT*
FROM tutorial.aapl_historical__stock_price
WHERE open > 550 OR close < 500;

Explanation:
--* Retrieves rows where `open` is greater than 550 or close is less than 500


Example 3: Using `NOT` Operator:
SELECT*
FROM tutorial.aapl_historical__stock_price
WHERE NOT (Year = 2014); 

Explanation:
--* WHERENOT (Year = 2014) exlcudes all rows where the year equals 2014.
    Instead, it retrieves rows here the year is any value other than 2014

##SPECIAL OPERATORS WITH THE WHERE CLAUSE: BETWEEN, LIKE  

Example 4: Using `BETWEEN` Special Operator:
SELECT date, open, close
FROM tutorial.aapl_historical_stock_price
WHERE close BETWEEN 500 AND 550;

Explanation: Retrieves rows where close is betweeen 500 AND 550


Example 5: Using `LIKE` with `_` character Special Operator:
SELECT*
FROM tutorial.aapl_historical_stock_price
WHERE date LIKE `1/_/14`

Explanation: retrieves rows where symbol matches the pattern `1/_14`.
The `_` wildcard in SQL is used with the `LIKE` operator to match exactly one character in a string. 




