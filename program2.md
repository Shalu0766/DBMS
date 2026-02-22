RETRIEVING DATA USING EMPLOYEE TABLE

#1. List all distinct jobs in Employee table
   
    SELECT DISTINCT job FROM Employee;

#2. List all information about employees in Department 30

   SELECT * FROM Employee WHERE deptno = 30;
  
#5. List Employee name, Employee number, Department of all clerks

    SELECT empno, ename, deptno FROM employee
    WHERE job = 'CLERK';

#3. Find all department numbers with department names greater than 20

    SELECT deptno FROM department WHERE deptno > 20;
    
#4. Find all information about managers and clerks in department 30

    SELECT * FROM employee
    WHERE deptno = 30 AND job IN ('MANAGER','CLERK');
    
#6. Find all managers NOT in department 30

    SELECT * FROM employee
    WHERE job = 'MANAGER' AND deptno <> 30;
    
