# SELECT and FROM Notes 

## Overview
The `SELECT` statement is used to specify the attributes to be returned by the query. `FROM` specifies the table from which to retrieve data. Together, they form the foundation of most SQL queries. 

## Example Queries and Explanations

#Example 1 Specific columns:  SELECT all columns 
``` sql
SELECT *
FROM aapl_historical_stock_price;

Explanation:
--SELECT* retrieves all columns from the appl_historical_stock_price;
-- * also known as wild character can be used to view all of the data of a SELECT statement


#Example 2 Specific columns: 
``` sql
SELECT date, close, volume
FROM aapl_historical_stock_price;

Explanation:
-- Here, SELECT date, close, volume retrieves only the specific columns


#Example 3 Aliases for specific column names
```sql
SELECT date AS "Trading Date", close AS "Closing Price"
FROM aapl_historical_stock_price;


Explanation:
AS is used to rename columns readabiliy within a SQL statement
In this case, date is displayed as "Trading Date" and close as "Closing Price" in the results


