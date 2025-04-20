# Data Engineer Journey

Hi I have started my journey to become data engineer from today. This file contain Week 1 Day 2 learning and inputs. Below are the topics i covered what i learned today


# Group By

I learn how to use group by query to use aggregate function based on specific column and getting filter it based on other columns 
Example
Select name,count(name) from table group by name
## Having Clause 

I learn how to use having and condition operator to filter data in the table query using group by 
some of the condition operator are like,between,=,!=,>,<,<=,>=,IN(), not in, not between
Example
Select name,count(name) as ct from table group by name having ct > 3
## CASE WHEN

I learn how to use case when with select query , aggregate function and with where condition
Example
Select column1,
case 
when condition then value
else value
end as columnname
from table 
## DATE functions (`YEAR`, `MONTH`)

I learn how use different date based function such as Month(),Year(),Now(),Day() etc.
## Nested subqueries

I learn how use nested query, how to apply join on nested query there execution order.
Example
Select sub.age from (select age, name from table where codition_1) sub
## Question Solved
I solved 2 question from stratascratch platform and 2 question from leetcode and 1 question from datalemur
##  Class Performance by Department

select max(sub.total_marks)- min(sub.total_mark) from
(
select (subject1mark+subject2mark+subject3mark) as total_marks from score_board
)sub 


## Number Of Units Per Nationality


SELECT host.nationality,
       COUNT(DISTINCT unit.unit_id) AS apartment_count
FROM airbnb_hosts host
JOIN airbnb_units unit
  ON host.host_id = unit.host_id
WHERE host.age < 30
  AND unit.unit_type = 'Apartment'
GROUP BY host.nationality
ORDER BY apartment_count DESC
LIMIT 1;


##  Employee Bonus
select name,bonus.bonus from employee left  join bonus on employee.empid = bonus.empid where bonus.bonus <  1000  or bonus.bonus is  null;
##  Combine Two Tables
select lastname,firstname,address.city,address.state from person left  join address on person.personId = address.personId;
##  Average Review Ratings
SELECT  DATE_PART('month', submit_date) as mth,product_id,Round(avg(stars),2) FROM reviews group by mth,product_id order by mth,product_id;

# Note
By this i end Week 1 Day 2. And will continue on the journey.