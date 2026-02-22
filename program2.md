RETRIEVING DATA USING EMPLOYEE TABLE

#1. List all distinct jobs in Employee table
   
    SELECT DISTINCT job FROM Employee;

#2. List all information about employees in Department 30

   SELECT * FROM Employee WHERE deptno = 30;
  
#5. List Employee name, Employee number, Department of all clerks

    SELECT empno, ename, deptno FROM employee
    WHERE job = 'CLERK';
