#🔹 RETRIEVING DATA – EMPLOYEE TABLE

#1. Employees who joined before 30-Jun-1980 OR after 31-Dec-1981

      SELECT * FROM employee
      WHERE hiredate < '1980-06-30' OR hiredate > '1981-12-31';

#2. Names of employees whose second alphabet is A

      SELECT ename FROM employee
      WHERE ename LIKE '_A%';
      
#3. Names of employees whose name is exactly 5 characters

      SELECT ename FROM employee
      WHERE LENGTH(ename) = 5;

#4. Names of employees whose second alphabet is A

      SELECT ename FROM employee
      WHERE ename LIKE '_A%';

#5. Employees NOT working as salesman, clerk or analyst

       SELECT ename FROM employee
       WHERE job NOT IN ('SALESMAN','CLERK','ANALYST');
