#🔹 RETRIEVING DATA – SET 2 (EMPLOYEE TABLE)

#1. Employees & jobs in Dept 30, ordered by salary (DESC)
  #📌 ORDER BY sal DESC → highest salary first

     SELECT ename, job, sal FROM employee
     WHERE deptno = 30 ORDER BY sal DESC;

#2. Job & DeptNo of employees
  #Name = 5 letters, starts with A and ends with N    _ → exactly one character

  SELECT job, deptno FROM employee
  WHERE ename LIKE 'A___N';
