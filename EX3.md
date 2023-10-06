# EX 3 SubQueries, Views and Joins 


## Create employee Table
```sql
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```
## Insert the values
```sql
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

## Create department table
```sql
CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));
```
## Insert the values in the department table
```sql
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');
```

### Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.


### QUERY:
![270762717-1848b392-372d-4111-af2d-25daf5458864](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/24498d8e-2c19-4472-8532-b2f8df73ed31)


### OUTPUT:
![270762784-ee7dd795-bf87-4dff-aca9-b80307477ddd](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/0a2cffe7-dc8d-409d-b266-a2309f6e6d06)

### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:
![270763155-2c78d720-f077-4843-bbbd-cefb0e36afcf](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/c6cc976f-3144-4af4-bec3-b9f5ca65cd40)


### OUTPUT:
![270763212-0ca9e7dc-c9b6-45c6-b7a0-bf123d815295](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/f5eebf00-0f98-428f-88b9-fc3ea1aabba1)

### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:

![270764132-ea1201a0-53bc-436b-b815-3889759afcff](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/9a54eb6e-4ab9-4e0a-9125-3711253e2954)

### OUTPUT:

![270764614-4c3e781f-8787-461d-b2ee-162f5222abd9](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/967951a0-c024-4c88-901e-e39d42763ded)


### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:
![270764614-4c3e781f-8787-461d-b2ee-162f5222abd9](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/a8928303-aaea-4a49-aef4-c68fb4b98b99)


### OUTPUT:
![270764656-753d1db9-8955-4b97-b850-43622886968b](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/50deda56-2647-43b2-bb04-609fad619ea0)

### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:
![270765070-3551ed65-3cb5-4846-b817-48436b507530](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/d9c74529-ba60-4447-a9a1-9867b3d4b43d)


### OUTPUT:
![270765159-026712b5-02b2-40d6-a757-cec5bc08890d](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/dd194de1-904a-40f4-b808-91eb35117fab)

### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:
![270767939-d83bbdcd-83a3-427e-bd2b-e799958b055d](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/f1726c2e-2db0-4a36-825e-3a97dec22264)


### OUTPUT:
![270767871-6941b531-33ed-41dc-b6f4-9e8bcc0dd113](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/892ad7ee-f247-4b64-9e1e-c99267c1d0d8)

## Create a Customer1 Table
```sql
CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);
```
## Inserting Values to the Table
```sql
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```
## Create a Salesperson1 table
```sql
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
## Inserting Values to the Table
```sql
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```
### Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

### QUERY:
![270771248-20c63405-1555-444c-8d92-daee8ad9f52d](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/6db77171-a303-47ee-a305-458031e57b0d)


### OUTPUT:
![270771306-4bf9b80e-b31d-486e-87b5-5462e60e6e2f](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/dda4317d-116b-41a6-945d-b7eff1ca805c)

### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:
![270772008-6b4b7f1a-e1fa-41eb-abfc-d544b005a00e](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/dfe8aba1-1bf8-4411-b085-4b924ad05eb1)


### OUTPUT:
![270772054-031553d8-640c-4306-9f12-cd4a6c6a68ed](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/c76c6fb1-1c72-4fcd-a75f-e916092f547d)

### Q9) Perform Natural join on both tables

### QUERY:
![270772360-a9609769-7404-4c74-909b-53d5610ea79a](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/f4d9fce9-6cd1-462d-a857-930f0d988a66)



### OUTPUT:
![270859730-099c0b7d-7822-4459-8025-92adc824dda8](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/48850bc3-a5ed-4287-a002-da1837366d67)

### Q10) Perform Left and right join on both tables

### QUERY:
### left join:
![270849330-7915ee92-d1e0-4528-be68-4bbe6fd7a11c](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/7b2331a3-98e1-43cf-a633-104299f852ca)
### right join:
![270860423-dcc24099-0fdd-404b-b81d-ea86de5cc8f9](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/c2caa697-e7de-4028-b68c-1b5553436169)

### OUTPUT:
### LEFT JOIN:

![270860293-7fe7c05b-ca77-4da2-9ab9-38a5f50a4879](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/5e32e485-70c7-4cb5-b94e-eabb9f5fd278)

### right join:
![270860293-7fe7c05b-ca77-4da2-9ab9-38a5f50a4879](https://github.com/22009011/EX-3-SubQueries-Views-and-Joins/assets/118343461/355f2759-cb68-4181-8a2f-a3ce38def468)
