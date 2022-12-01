
# Oracle: LISTAGG(input_string, separator); Sql Server: string_agg() 

 聚合函数，以某字段作为主字段，合并另一字段，可定义链接符号；
 

LISTAGG(input_string, separator)
```sql
select 
    Name, 
    listagg(PhoneNumber,',')
        within group (order by Name) PhoneNumber
from 
    PersonInFo
where 
    Name='Yvonne'
group by 
    Name;
```

string_agg()
```sql
SELECT
    city, 
    STRING_AGG(email,';') 
        WITHIN GROUP (ORDER BY email) email_list
FROM
    sales.customers
GROUP BY
    city;
```



