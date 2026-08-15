**CREATE TABLE**

```sql
-- Creates the initial student table with primary key, nullability, dynamic default values, and check constraints
CREATE TABLE student (
    student_id INT PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    date_of_birth DATE,
    gpa DECIMAL(3, 2) CHECK (gpa >= 0.00 AND gpa <= 4.00),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

```

**ALTER TABLE (Structure Modifications)**

```sql
-- 1. Add a new column to track student major
ALTER TABLE student
ADD major VARCHAR(50);

-- 2. Modify an existing column to expand character limit
ALTER TABLE student
MODIFY COLUMN email VARCHAR(150);

-- 3. Add a dynamic constraint (e.g., set default value for a new column)
ALTER TABLE student
ADD status VARCHAR(20) DEFAULT 'Active';

-- 4. Drop a column from the table
ALTER TABLE student
DROP COLUMN date_of_birth;

```

**RENAME TABLE**

```sql
-- Renames the student table to a new entity name
ALTER TABLE student
RENAME TO registered_students;

```

**TRUNCATE TABLE**

```sql
-- Empties all records while preserving the table structure and indexes
TRUNCATE TABLE student;

```

**DROP TABLE**

```sql
-- Permanently deletes the table structure, constraints, and all data
DROP TABLE student;

```

---
