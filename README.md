# SQL

# Window Function
### It applies on aggregates, ranking  and analytics function over a particular window. {aggregates(Sum,Avg,Count,Min,Max), Ranking(Row_Number, Rank, Dense_Rank,Percent_Rank),Analytic(LEAD,LAG,First_Value,Last_Value)}

# Sysntax Of Window Function
```sql
select Column_names(s),
fun() over (
              [partition by]
              [order by]
                )
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

