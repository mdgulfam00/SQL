# SQL

# Case Statement
```sql
select age,
case
when age>25 then 'OverAge'
when age<25 then 'Underage'
else 'Normal Age'
end as category
from Customers;
```

