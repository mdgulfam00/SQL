# SQL

# Window Function
#### It applies on aggregates, ranking  and analytics function over a particular window. {aggregates(Sum,Avg,Count,Min,Max), Ranking(Row_Number, Rank, Dense_Rank,Percent_Rank),Analytic(LEAD,LAG,First_Value,Last_Value)}

# Syntax Of Window Function
```sql
select Column_names(s),
fun() over (
              [partition by]
              [order by]
                )
```
# Syntax of Window Function on Agrregate functions
```sql
select country,age ,
sum(age) over(partition by country) as 'Sum',
avg(age) over(partition by country) as 'Avg',
min(age) over(partition by country) as 'Min',
max(age) over(partition by country) as 'Max',
count(age) over(partition by country) as 'Count'
from Customers;
```
# Sysntax of Window Function on Ranking functions
```sql
select country,
row_Number() over(order by country) as 'Row Number',
rank() over(order by country) as 'Rank',
dense_rank() over(order by country) as 'Dense rank',
percent_rank() over(order by country) as 'Percent rank'
from customers;
```
### Rank() -> will skip the rank as many times as it duplicates where as Dense_Rank()-> will not skip anything it will rank equal items same and then give rank to next item by previous rank + 1

# Syntax of Window function on Analytics Functions
```sql
select country,
first_value(country) over (order by country) as 'First value',
last_value(country) over (order by country) as 'Last value',
lead(country) over (order by country) as 'Lead',
lag(country) over (order by country) as 'Lag'
from customers;
```
### we can pass an argument to lead() and lag() function for number of lead and number of lags to be occured.

```sql
 Select country,
lead(country,2) over (order by country) as 'Lead', --It will lead by 2 and give result which is present at 2 distance below it.
lag(country ,2) over (order by country) as 'Lag'   --It will lag by 2 and give result which is present at 2 distance above it.
```


# Case Statement
### It is used to check conditions based on requirement on columns
```sql
select age,
case
when age>25 then 'OverAge'
when age<25 then 'Underage'
else 'Normal Age'
end as category
from Customers;
```

# Case Expression
### It is used to give hardcoded value on a coulumn as expression for output

```sql
select age,
case country
when 'USA' then 'Good'
when 'UK' then 'Very Good'
else 'Normal'
end as category
from Customers;
```

