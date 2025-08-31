# Employee Database SQL Practice

## Project Description
This project is a **sample Employee Database** designed for practicing a wide range of **SQL queries and conditions**.  
It is my **third SQL project** and helps learners understand how to:

- Create a database and tables  
- Insert and manage data  
- Filter data using `WHERE`, `LIKE`, `BETWEEN`, `IN`  
- Use logical operators like `AND` and `OR`  
- Sort data using `ORDER BY`  
- Perform updates and transactions  

The database contains **20 employees** with different roles, ages, salaries, and join dates, allowing practice with multiple real-world scenarios.

## Complete SQL Code (All-in-One)

```sql
-- Create Database and Table
CREATE DATABASE EmployeesDB;
USE EmployeesDB;

CREATE TABLE Employees (
    EmployeeID int,
    Name VARCHAR(50),
    Age int,
    Role VARCHAR(50),
    Salary int,
    JoinDate DATE
);

-- Insert Sample Data
INSERT INTO Employees (EmployeeID, Name, Age, Role, Salary, JoinDate) VALUES
(1, 'John Smith', 28, 'Software Engineer', 75000, '2022-03-15'),
(2, 'Ali Khan', 32, 'Data Analyst', 68000, '2021-07-10'),
(3, 'Michael Johnson', 25, 'Intern', 20000, '2023-06-01'),
(4, 'Ayesha Malik', 40, 'Project Manager', 120000, '2019-11-20'),
(5, 'William Brown', 30, 'AI Engineer', 95000, '2020-05-05'),
(6, 'Hina Siddiqui', 29, 'UI/UX Designer', 70000, '2021-09-14'),
(7, 'James Davis', 35, 'Database Administrator', 105000, '2020-01-20'),
(8, 'Zara Iqbal', 27, 'Web Developer', 60000, '2022-11-10'),
(9, 'David Miller', 31, 'Network Engineer', 85000, '2019-06-25'),
(10, 'Fatima Noor', 26, 'Content Writer', 45000, '2023-04-12'),
(11, 'Robert Wilson', 38, 'Team Lead', 110000, '2018-12-01'),
(12, 'Nadia Jamil', 33, 'Business Analyst', 88000, '2020-08-07'),
(13, 'Daniel Anderson', 29, 'Mobile App Developer', 72000, '2021-03-19'),
(14, 'Maryam Shah', 24, 'Intern', 18000, '2023-07-02'),
(15, 'Christopher Taylor', 36, 'DevOps Engineer', 99000, '2019-05-17'),
(16, 'Iqra Hanif', 28, 'Software Tester', 65000, '2022-01-09'),
(17, 'Matthew Thomas', 41, 'Senior Architect', 130000, '2017-10-15'),
(18, 'Aiman Rafiq', 34, 'HR Manager', 78000, '2019-09-30'),
(19, 'Andrew Harris', 27, 'Graphic Designer', 55000, '2022-06-20'),
(20, 'Salman Tariq', 39, 'Product Owner', 115000, '2018-02-11');

-- Select All
SELECT * FROM Employees;

-- Conditions / Queries
SELECT * FROM Employees WHERE Age > 30;
SELECT * FROM Employees WHERE Age < 30;
SELECT * FROM Employees WHERE Salary > 104000;
SELECT * FROM Employees WHERE Salary LIKE 75000;
SELECT * FROM Employees WHERE Name LIKE 'A%';
SELECT * FROM Employees WHERE Name LIKE '%n';
SELECT * FROM Employees WHERE JoinDate BETWEEN '2020-01-01' AND '2021-12-31';
SELECT * FROM Employees WHERE Role IN ('AI Engineer', 'Data Analyst');
SELECT * FROM Employees WHERE Age > 25 AND Salary > 60000;
SELECT * FROM Employees WHERE Age > 30 AND Salary > 90000;
SELECT * FROM Employees WHERE Age < 30 OR Salary < 50000;
SELECT * FROM Employees ORDER BY Salary DESC;
SELECT * FROM Employees ORDER BY Name ASC;
SELECT * FROM Employees ORDER BY Age ASC;
SELECT * FROM Employees WHERE Salary > 70000 AND (Role = 'AI Engineer' OR Role = 'Data Analyst');
SELECT * FROM Employees WHERE Role NOT LIKE 'Intern';
SELECT * FROM Employees WHERE Role NOT IN ('Intern', 'Content Writer');

-- Update Example
UPDATE Employees
SET Salary = 80000
WHERE Name = 'John Smith';

-- Transaction Example
BEGIN TRANSACTION;
ROLLBACK;
