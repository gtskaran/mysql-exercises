**INSERT Queries**

1. *Insert a single record with explicit column names:*
```sql
INSERT INTO student (student_id, first_name, last_name, email, date_of_birth, gpa)
VALUES (21, 'Oliver', 'White', 'oliver.w@example.com', '2002-03-14', 3.75);

```


2. *Insert multiple records in a single statement:*
```sql
INSERT INTO student (student_id, first_name, last_name, email, date_of_birth, gpa) VALUES
(22, 'Sophia', 'Harris', 'sophia.h@example.com', '2003-08-22', 3.88),
(23, 'Daniel', 'Clark', 'daniel.c@example.com', '2001-10-05', 3.12);

```


3. *Insert partial data (excluding optional/nullable columns like GPA):*
```sql
INSERT INTO student (student_id, first_name, last_name, email, date_of_birth)
VALUES (24, 'Chloe', 'Lewis', 'chloe.l@example.com', '2002-12-19');

```



---
