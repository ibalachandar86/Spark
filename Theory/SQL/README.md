# Entity Relationship diagram (ER)

# Select specific (where) details
select * from car where production_year=1999;

# Less than Greater than Operators
 -. < (less than)
 -. > (greater than)
 -. <= (less than or equal)
 -. >= (greater than or equal)
 -. <>	Not equal. Note: In some versions of SQL this operator may be written as !=	
 -. BETWEEN	Between a certain range	
 -. LIKE Search for a pattern	
 -. IN	To specify multiple possible values for a column
select * from car where price > 10000;

# -------------------------- Queries --------------------------
https://www.w3schools.com/sql/default.asp
# Select
select * from Customers;
select CustomerID,CustomerName from Customers;
Columns: CustomerID,CustomerName,ContactName,Address,City,PostalCode,Country
# Where
select * from Customers where CustomerID < 25;
select * from Customers where CustomerID <> 25;
select * from Customers where CustomerID between 25 and 30;
select * from Customers where CustomerName like "%rank%";
# AND OR NOT
select * from Customers where Country in ("Germany","Mexico");
select * from Customers where NOT Country = "Germany";
select * from Customers where CustomerName like "A%" AND Country = "Germany";
select * from Customers where Country in ("Sweden", "France") OR CustomerName like "A%";
# Order By
select * from Customers order by Country asc, CustomerName desc;
# Insert into (Remember keyword values)
insert into Customers values (92,"bala","chandar","abc","chennai","600021","India");
insert into Customers (CustomerID,CustomerName,Country) values (93,"jwala","India");
select * from Customers where ContactName is NULL;
select * from Customers where ContactName is not NULL;
# Update  (Remember keyword Set)
update Customers SET ContactName = NULL where CustomerID = 92;
# Delete  (Remember Delete from)
delete from Customers where CustomerID = 93;
# Limit/Top
select * from Customers limit 5;
SELECT TOP 3 * FROM Customers;
# Min/Max/Count/Avg/Sum
select min(CustomerID) FROM Customers;
select max(CustomerID) FROM Customers;
select count(Country) FROM Customers;
select avg(CustomerID) FROM Customers;
select sum(CustomerID) FROM Customers;
# LIKE Operator	Description + Wildcard characters
# WHERE CustomerName LIKE 'a%'	Finds any values that start with "a"
# WHERE CustomerName LIKE '%a'	Finds any values that end with "a"
# WHERE CustomerName LIKE '%or%'	Finds any values that have "or" in any position
# WHERE CustomerName LIKE '_r%'	Finds any values that have "r" in the second position
# WHERE CustomerName LIKE 'a_%'	Finds any values that start with "a" and are at least 2 characters in length
# WHERE CustomerName LIKE 'a__%'	Finds any values that start with "a" and are at least 3 characters in length
# WHERE ContactName LIKE 'a%o'	Finds any values that start with "a" and ends with "o"
select * from Customers where CustomerName like "A%";
select * from Customers where CustomerName like "%n";
select * from Customers where CustomerName like "B___%";
select * from Customers where CustomerName like "C%a_";
# ----------------------------------------------------------------
