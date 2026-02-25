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

#2. Display your age in days

         SELECT DATEDIFF(CURDATE(), '2000-01-01') AS age_in_days;

#3. Display your age in months

         SELECT TIMESTAMPDIFF(MONTH, '2000-01-01', CURDATE()) AS age_in_months;

#4. Display current date as 15th August Friday Nineteen Ninety-Seven

           SELECT DATE_FORMAT('1997-08-15', '%D %M %W %Y') AS formatted_date;

#5. Display formatted output for each employee as Scott joined company on Wednesday 13th August Nineteen Ninety

             SELECT CONCAT(
               ename,' has joined the company on ',
               DATE_FORMAT(hiredate,'%W %D %M %Y')
               ) AS joining_info FROM employee
               WHERE ename = 'SCOTT';

#6. Find nearest Saturday after current date

            SELECT DATE_ADD(CURDATE(), INTERVAL (7 - DAYOFWEEK(CURDATE())) DAY) AS next_saturday;

#7. Display current time

            SELECT CURTIME();

#8. Display the date three months before current date

             SELECT DATE_SUB(CURDATE(), INTERVAL 3 MONTH);

#9. Employees who joined in the month of December

              SELECT ename, hiredate FROM employee
              WHERE MONTH(hiredate) = 12;

#10. Employees whose first 2 characters of hiredate = last 2 characters of salary

              SELECT ename FROM employee
              WHERE LEFT(YEAR(hiredate),2) = RIGHT(sal,2);

              
