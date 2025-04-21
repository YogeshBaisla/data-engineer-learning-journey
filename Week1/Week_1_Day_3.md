# Data Engineer Journey

Hi I have started my journey to become data engineer from today. This file contain Week 1 Day 3 learning and inputs. Below are the topics i covered what i learned today


# Inner Join

I learn how to use inner join and what is the use case of inner join
Example
Select a.column1,b.clumn2 from a inner join a.id = b.id;
## Left Join

I learn how to use left join and what is the use case of inner join
Example 
Select a.column1,b.clumn2 from a left join a.id = b.id;
## Right Join

I learn how to use right join and what is the use case of inner join
Example 
Select a.column1,b.clumn2 from a right join a.id = b.id;
## Full Join

I learn how to use full join and what is the use case of inner join
Example 
Select a.column1,b.clumn2 from a full join a.id = b.id;
## Is Null/Is Not Null

I learn how use is null/is not null with where condition to handle null values
Example
Select a.column1,b.clumn2 from a left join a.id = b.id where b.id is null;

## Question Solved
I solved 2 question from Leetcode platform and 1 question from datalemur
##  Customers Who Never Order

select name as Customers from customers left  join orders on customers.id = orders.customerId where orders.customerId is  null


## Department Highest Salary


select Department,Employee,Salary from  (select department.name as Department,employee.name as Employee,employee.salary as Salary,(DENSE_RANK()  over  (partition  by department.name order  by employee.salary desc))  as rk from department inner  join employee on department.id = employee.departmentId) sub where sub.rk =1;


##  Page With No Likes
SELECT pages.page_id FROM pages left join page_likes on pages.page_id = page_likes.page_id where page_likes.page_id is null order by pages.page_id asc;


# Note
By this i end Week 1 Day 3. And will continue on the journey.