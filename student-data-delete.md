**DELETE Queries**

1. *Delete a single record by Primary Key:*
```sql
DELETE FROM student
WHERE student_id = 20;

```


2. *Delete records matching a threshold condition:*
```sql
DELETE FROM student
WHERE gpa < 2.85;

```


3. *Delete records based on a date condition:*
```sql
DELETE FROM student
WHERE date_of_birth < '2001-06-01';

```

---
