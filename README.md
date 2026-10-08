# MySql-Workbench.connect
USE classicmodels;
SELECT paymentDate, SUM(amount) AS total_amount
FROM payments
GROUP BY paymentDate
ORDER BY paymentDate DESC
LIMIT 5;
SUM(amount)
GROUP BY paymentDate
ORDER BY paymentDate DESC
LIMIT 5
SELECT customerName, country, AVG(creditLimit) AS average_credit_limit
FROM customers
GROUP BY customerName, country;
AVG(creditLimit)
GROUP BY customerName, country
quantityOrdered × priceEach
SUM(quantityOrdered * priceEach)
SELECT 
    productCode,
    quantityOrdered,
    SUM(quantityOrdered * priceEach) AS total_price
FROM orderdetails
GROUP BY productCode, quantityOrdered;
quantityOrdered * priceEach
GROUP BY productCode, quantityOrdered
SELECT checkNumber, MAX(amount) AS highest_amount
FROM payments
GROUP BY checkNumber;
MAX(amount)
GROUP BY checkNumber
-- Question 1
SELECT paymentDate, SUM(amount) AS total_amount
FROM payments
GROUP BY paymentDate
ORDER BY paymentDate DESC
LIMIT 5;


-- Question 2
SELECT customerName, country, AVG(creditLimit) AS average_credit_limit
FROM customers
GROUP BY customerName, country;


-- Question 3
SELECT 
    productCode,
    quantityOrdered,
    SUM(quantityOrdered * priceEach) AS total_price
FROM orderdetails
GROUP BY productCode, quantityOrdered;


-- Question 4
SELECT checkNumber, MAX(amount) AS highest_amount
FROM payments
GROUP BY checkNumber;
| Question | Main function | Main concept |
|---|---|---|
| 1 | `SUM()` | `GROUP BY`, `ORDER BY`, `LIMIT` |
| 2 | `AVG()` | `GROUP BY` |
| 3 | `SUM()` | Calculation + `GROUP BY` |
| 4 | `MAX()` | `GROUP BY` |
