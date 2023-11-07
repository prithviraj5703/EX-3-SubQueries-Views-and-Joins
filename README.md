# EX-3-SubQueries, Views and Joins
# DATE:18.8.2023
# Create employee Table
```
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```
# Insert the values
```
INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7369, 'SMITH', 'CLERK', 7902, '17-DEC-80', 800, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-81', 1600, 300, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7521, 'WARD', 'SALESMAN', 7698, '22-FEB-81', 1250, 500, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7566, 'JONES', 'MANAGER', 7839, '02-APR-81', 2975, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-81', 1250, 1400, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7698, 'BLAKE', 'MANAGER', 7839, '01-MAY-81', 2850, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7782, 'CLARK', 'MANAGER', 7839, '09-JUN-81', 2450, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7788, 'SCOTT', 'ANALYST', 7566, '19-APR-87', 3000, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7839, 'KING', 'PRESIDENT', NULL, '17-NOV-81', 5000, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7844, 'TURNER', 'SALESMAN', 7698, '08-SEP-81', 1500, 0, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7876, 'ADAMS', 'CLERK', 7788, '23-MAY-87', 1100, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7900, 'JAMES', 'CLERK', 7698, '03-DEC-81', 950, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('03-DEC-81', 'DD-MON-RR'), 3000, 20, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('23-JAN-82', 'DD-MON-RR'), 1300, 10, 10);
```
# Create department table
```
CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));
```
# Insert the values in the department table
```
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');
```
# Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.

# QUERY:

![270762717-1848b392-372d-4111-af2d-25daf5458864](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/41f5451b-c769-4704-8c05-466b2ea5705b)


# OUTPUT:

![270762784-ee7dd795-bf87-4dff-aca9-b80307477ddd](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/ffdaea81-2b63-4ae7-be46-1e67bb6b7ae2)


# Q2) List the ename,job,sal of the employee who get minimum salary in the company.

# QUERY:

![270763155-2c78d720-f077-4843-bbbd-cefb0e36afcf](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/41af8b91-9ad8-46bf-9b61-4cc96d0f30be)

# OUTPUT:

![270763212-0ca9e7dc-c9b6-45c6-b7a0-bf123d815295](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/61246c08-0915-4ae9-a351-b67d9d0ec4f6)


# Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

# QUERY:

![270764132-ea1201a0-53bc-436b-b815-3889759afcff](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/297633e9-4d52-41c7-850b-84640991d179)


# OUTPUT:

![270764187-7376ae95-bab6-4739-abd7-bdc5e8a727dd](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/c41afc3f-efaa-4eae-8fbe-747b7f83642a)


# Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

# QUERY:

![270764614-4c3e781f-8787-461d-b2ee-162f5222abd9](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/f53a111b-547a-462c-b2d0-31c36987c61b)


# OUTPUT:

![270764656-753d1db9-8955-4b97-b850-43622886968b](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/d06e2364-73cb-447b-83b9-104d1c89177c)


# Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

# QUERY:

![270765070-3551ed65-3cb5-4846-b817-48436b507530](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/6aace481-6fa2-45b0-b328-a3ef5d0b3c27)


# OUTPUT:

![270765159-026712b5-02b2-40d6-a757-cec5bc08890d](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/7e090e1e-1d01-4abd-8009-2523f71fdbf8)


# Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

# QUERY:

![270767939-d83bbdcd-83a3-427e-bd2b-e799958b055d](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/2e3ea98f-3d15-4b4b-8cb4-f4b57af3237c)



# OUTPUT:

![270767871-6941b531-33ed-41dc-b6f4-9e8bcc0dd113](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/d2fdab84-3b35-45ba-a001-0d7256df9bb3)


# Create a Customer1 Table
```
CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);
````
# Inserting Values to the Table
```
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```
# Create a Salesperson1 table
```
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
# Inserting Values to the Table
```
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```
# Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

# QUERY:

![270771248-20c63405-1555-444c-8d92-daee8ad9f52d](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/ea7f972a-fc23-43aa-b8ea-9b0e573a4521)


# OUTPUT:


![270771306-4bf9b80e-b31d-486e-87b5-5462e60e6e2f](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/ab681be5-721d-452c-8f1e-d727438535ae)


# Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.

# QUERY:

![270772008-6b4b7f1a-e1fa-41eb-abfc-d544b005a00e](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/98b9ff26-e478-4e16-a4cd-e2176bb5f457)


# OUTPUT:

![270772054-031553d8-640c-4306-9f12-cd4a6c6a68ed](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/860d4ed6-0b5e-47b0-ae88-3c29883d6425)


# Q9) Perform Natural join on both tables

# QUERY:

![270772360-a9609769-7404-4c74-909b-53d5610ea79a](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/3bcc87af-430b-48f6-b693-2a41ad596039)


# OUTPUT:

![270772421-1026e100-8a70-45e8-bdcb-3d51efdfa1fc](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/ba6a303d-ce30-4ce2-aab4-5e581ce64d35)


# Q10) Perform Left and right join on both tables

# QUERY:

# Left Join

![270849330-7915ee92-d1e0-4528-be68-4bbe6fd7a11c](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/d61e0543-c7a1-4964-8860-d4c92dcfc592)



# Right join
```
![image](https://github.com/DhanushPalani/EX-3-SubQueries-Views-and-Joins/assets/121594640/8be146f2-c02a-4c31-8dd7-a759a92e69c3)
```
# OUTPUT:

# Left Join

![270773161-f7e2b17f-33d1-404c-8a43-83636dc8c552](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/8f227fff-a1bf-4d87-830e-e8c18b62216d)

# Right Join

![270773439-43cc7093-35af-4c4b-8854-068a0f0b34d1](https://github.com/prithviraj5703/EX-3-SubQueries-Views-and-Joins/assets/121418418/5e2694c1-1a6d-4549-9a4c-76f77658b176)


# RESULT:
Output is sucessfully got.
