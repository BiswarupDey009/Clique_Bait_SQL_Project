1) Your task is to determine the number of unique users who accessed the website.

<details>
<summary>Click to expand the Answer!</summary>
  
```sql
select count(distinct user_id) from users;
```
</details>


|count(distinct user_id)|
|-----------------------|
|500|

2) Your task is to calculate the average number of cookies all users have on the platform?
<details>
<summary>Click to expand the Answer!</summary>

sql
with cte as(
select user_id,count(cookie_id) as cc  from users
group by user_id
) 
select round(avg(cc)) average_cookies_per_user
from cte ;

</details>

|average_cookies_per_user | 
|-------------------------|
|4|

3) Your role is to derive the unique number of visits by all users for each month?
<details>
<summary>Click to expand the Answer!</summary>
  
sql
select month(event_time) Month,
count(distinct visit_id) unique_visit_count
from events
where event_type=1
group by Month;

</details>

|Month|unique_visit_count|
|---------------|---------|
|1	|876|
|2	|1488|
|3	|916|
|4	|248|
|5	|36|
