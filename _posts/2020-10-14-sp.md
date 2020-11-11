# Keep these things in mind when you start to create SP

Before to discuss the points we just go through what is stored procedure and where its used. 

When we are using SQL as a back-end we need some queries frequently used in our application. Here we have to go stored procedures, we can save the query as Stored procedure and we can use where ever we want over and over again.

While creating stored procedure we should keep some standards for more efficiency.

  

### Use (nolock)

Normally (nolock) is not a necessary one, but without (nolock) sometimes we might face timeout issues in our application.

For example, we are in the middle of some transaction, SQL locks the table until the traction ends. At that time if our SP runs SQL prevents all other operations, So we couldn't get the result. 

we can overcome the above problem by using (nolock), Where ever you used SQL table in your procedure you just add (nolock) after that as a best practice.

```sql
select * from tbl_employeemaster (nolock)
```

### Don't Nested

Nested SP makes more complex to fine error. 

     Avoid multiple sp too 

Nested Stored procedure 

### Select specific Columns

Use transactions

Maintain blocks
