Ending with vowel:--
select distinct city from station where REGEXP_LIKE(LOWER(CITY), '[aeiou]$');

Does not start and end with vowel
SELECT DISTINCT city
FROM   station
WHERE REGEXP_LIKE(city, '^[^aeiouAEIOU].*[^aeiouAEIOU]$')


There is an EMPLOYEE table and DEPARTMENT table where deptid is the foreign key in employee table . write a sql query to display department names along with no of employees working in it.

Ans-> Select deptName, count(*) from Departments inner join Employee on Employee.deptid=Departments.deptid group by Departments.deptid order by Departments.deptName


MYSQL ASSIGNMENT----------
------------------------------

create table Student(
registration_No Integer(4), student_name varchar(20), student_score Integer(3)
);

create table Course(
course_name varchar(20),semester varchar(10)
);

Alter table Course Add CONSTRAINT p_k PRIMARY KEY(course_name);

Alter table Student Add Column course_name varchar(20) references Course(course_name);

Insert Into Course values ("Unix OS","Sem 2"),("SQL PL/SQL","Sem 3"),("Java","Sem 2");

Insert into Student values (1011,"Raju Kumar",40,"Unix OS"),(1023,"Nancy J",67,"Unix OS"),(1899,"Viraj",59,"Java");
--select student_name from Student where student_score>=50;
--select registration_No,student_name,Student.course_name,semester from Student,Course where Student.course_name=Course.course_name;
--select course_name from Course where course_name not in(select course_name from Student);
--select student_name,count(*) as No_of_Courses from Student group by student_name;
--select course_name, count(*) as "Student Count" from Student group by course_name;
