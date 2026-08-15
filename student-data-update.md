**UPDATE Queries**

1. *Update a specific record using the Primary Key:*
```sql
UPDATE student
SET gpa = 3.95
WHERE student_id = 1;

```


2. *Update multiple records based on a range condition:*
```sql
UPDATE student
SET gpa = gpa + 0.10
WHERE gpa < 3.00;

```


3. *Update a string field using a matching text condition:*
```sql
UPDATE student
SET email = 'liam.smith.updated@example.com'
WHERE last_name = 'Smith' AND first_name = 'Liam';

```



---
