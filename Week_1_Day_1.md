# Data Engineer Journey

Hi I have started my journey to become data engineer from today. This file contain Week 1 Day 1 learning and inputs. Below are the topics i covered what i learned today


# Select Query

I learn how to use select query to fetch all or limited column data
Example
Select * from table
Select column1,column2 from table
## Where and Condition operator

I learn how to use where and condition operator to filter data in the table
some of the condition operator are like,between,=,!=,>,<,<=,>=,IN(), not in, not between
Example
Select * from table where column1 = 'x' and column2 between x and y;
## Distinct, Order by

I learn how to fetch distinct data from table and how to order them based on specific column in desire order.
Example 
Select Distinct column1 from table order by column1 asc.
## Limit and Offset

I learn how to limit number record to fetch from table and how to fetch next subset from sequence.
Example
Select * from table limit 5 offset 10 
## Question Solved
I solved 3 question from stratascratch platform 
##  Most Lucrative Products

select product_id,sum(units_sold*cost_in_dollars) as revenue from online_orders where date_sold between '2022-01-01' and '2022-06-30' group by product_id order by revenue desc limit 5;


## April Admin Employees


select count(*) from worker where department = 'Admin' and Month(joining_date) >= 4;

##  Workers by Department Since April

select department,count(*) as num_workers from worker where joining_date > '2014-04-01' group by department order by num_workers desc;

# Note
By this i end Week 1 Day 1. And will continue on the journey.