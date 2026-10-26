---1.
create or replace table work (
    id STRING,
    first_name STRING,
    last_name STRING,
    department STRING,
    salary STRING,
    hire_data DATE,
    city STRING

);
insert into work values 
('1','Alice','Green','IT','70000', DATE'2020-01-10','Johannesburg'),
('2','Brian','Lee','HR','45000', DATE'2019-03-22','Cape Town'),
('3','Cathy','Zulu','Finance','65000', DATE'2018-07-18','Durban'),
('4','David','Mokoena','Marketing','50000', DATE'2021-11-05','Pretoria'),
('5','Eva','Naidoo','IT','72000', DATE'2017-09-30','Johannesburg');
select* from work;
---2.
select distinct(department)
from work;
---3. 
select first_name,
       last_name
from work
order by salary desc;
---4.
select id,
       first_name,
       last_name,
       salary
from work
order by salary desc
limit 3;
---5.
select id,
       first_name,
       last_name,
       department
from work
where department = 'IT';
---6.
select id,
       first_name,
       last_name,
       department,
       salary
from work
where department = 'Finance' and salary>60000;
---7. 
select id,
       first_name,
       last_name,
       department
from work
where department = 'HR' or department = 'Marketing';
---8.
select id,
       first_name,
       last_name,
       department
from work
where department <> 'IT';
---9.
select id,
       first_name,
       last_name,
       department
from work
where department in ('IT', 'HR', 'Finance');
---10.
select id,
       first_name,
       last_name,
       department,
       salary,
       city
from work
where department = 'IT' and salary > 65000 and city = 'Johannesburg';
