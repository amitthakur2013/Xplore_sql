Ending with vowel:--
select distinct city from station where REGEXP_LIKE(LOWER(CITY), '[aeiou]$');

Does not start and end with vowel
SELECT DISTINCT city
FROM   station
WHERE REGEXP_LIKE(city, '^[^aeiouAEIOU].*[^aeiouAEIOU]$')


There is an EMPLOYEE table and DEPARTMENT table where deptid is the foreign key in employee table . write a sql query to display department names along with no of employees working in it.

Ans-> Select deptName, count(*) from Departments inner join Employee on Employee.deptid=Departments.deptid group by Departments.deptid order by Departments.deptName
