#🔹 RETRIEVING DATA

#1. Display empno, ename, dept name instead of deptno

        SELECT e.empno, e.ename,
        CASE e.deptno
             WHEN 10 THEN 'RESEARCH'
             WHEN 20 THEN 'ACCOUNTING'
             WHEN 30 THEN 'SALES'
             WHEN 40 THEN 'OPERATIONS'
        END AS department
        FROM employee e;

