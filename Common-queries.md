# Data Manipulation Language
C - INSERT
R - SELECT
U - UPDATE
D - DELETE
Reference: w3schools.com
## 1. SELECT
SELECT *column1, column2,* ...  
FROM *table_name*;

SELECT * FROM Orders;  
selects all columns from "Orders" table

### 1.1 SELECT DISTINCT
* only distinct values returned  
SELECT DISTINCT Country 
FROM Orders;
* Useful for couting unique values  
SELECT COUNT(DISTINCT Country) FROM Customers;
## 1.2 SQL ORDER BY
SELECT *column1,* ...  
FROM *table*  
ORDER BY *column1,* ... ASC|DESC

SELECT *   
FROM Orders  
ORDER BY Country, City;
* If orders have same country will sort by city
## 2. SQL WHERE
Used for conditions  
SELECT *column1,* ...  
FROM *table*  
WHERE *condition*;  

SELECT *  
FROM Orders  
WHERE Country='Mexico'
### 2.1 SQL AND, OR and NOT
SELECT *  
FROM Orders  
WHERE NOT Country='Mexico' AND (Order-ID <= 30 OR Order-ID >= 78)  
Operators: https://www.w3schools.com/sql/sql_where.asp

## 3 INSERT INTO
INSERT INTO *table_name* (*column1, column2,* ...)  
VALUES (*value1, value2,* ...)
* for all columns do not need to specify which column
  * make sure values are entered in the correct order (2nd value corresponds to 2nd column)  
  
INSERT INTO Customers (CustomerName, City, Country)  
VALUES ('Cardinal', 'Stavanger', 'Norway');  

