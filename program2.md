RETRIEVING DATA USING EMPLOYEE TABLE

#1. List all distinct jobs in Employee table
   
    SELECT DISTINCT job FROM Employee;

#2. List all information about employees in Department 30

  SELECT * FROM Employee WHERE deptno = 30;

#3. Find all department numbers with department names greater than 20

  SELECT deptno FROM department WHERE deptno > 20;

#4. Find all information about managers and clerks in department 30

  SELECT * FROM employee
  WHERE deptno = 30 AND job IN ('MANAGER','CLERK');
  
