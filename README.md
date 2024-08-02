# SQL

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

