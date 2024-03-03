1) Your task is to determine the number of unique users who accessed the website.

<details>
<summary>Click to expand the Answer!</summary>
  
sql
select count(distinct user_id) from users;

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
