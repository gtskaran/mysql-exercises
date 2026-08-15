**SELECT Queries**

1. *Select all fields for students with a GPA higher than 3.70:*
```sql
SELECT * FROM student
WHERE gpa > 3.70;

```


2. *Select specific columns for students born after January 1, 2003:*
```sql
SELECT first_name, last_name, email 
FROM student
WHERE date_of_birth > '2003-01-01';

```


3. *Select using multiple criteria (AND condition):*
```sql
SELECT student_id, first_name, gpa 
FROM student
WHERE gpa >= 3.50 AND date_of_birth >= '2002-01-01';

```



---
