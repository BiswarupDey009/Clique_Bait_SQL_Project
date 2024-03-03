1) Your task is to determine the number of unique users who accessed the website.

<details>
<summary>Click to expand the Answer!</summary>
  
sql
select count(distinct user_id) from users;

</details>


|count(distinct user_id)|
|-----------------------|
|500|
