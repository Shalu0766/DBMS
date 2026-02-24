# 1. Create Database

     CREATE DATABASE one1;
     USE one1;

#2. Create DEPARTMENT table

      
     CREATE TABLE department (
        deptno INT (2) PRIMARY KEY,
        dname VARCHAR(15) NOT NULL
     );

# 3. Create EMPLOYEE table

     CREATE TABLE employee (
        empno INT(4) PRIMARY KEY,
        ename VARCHAR(20) NOT NULL,
        job VARCHAR(20),
        mgr INT(4),
        hiredate DATE,
        sal DECIMAL(10,0),
        comm DECIMAL(7,0),
        deptno INT(2),
        FOREIGN KEY (deptno) REFERENCES department(deptno)
      );

      
