## **PRODUCTS TABLE DATA**

| **Product_id** | **Description** | **Quantity** | **Price** |
| --- | --- | --- | --- |
| 1004 | 4GB DDR4 RAM | 5 | 1100 |
| 1005 | ASUS M5A78L-M Motherboard | 2 | 9852 |
| 1006 | Gigabyte N3050M Motherboard | 5 | 4890 |
| 1007 | Gigabyte 78LMT Motherboard | 2 | 6800 |
| 1008 | Dell 21.5 Inch LED Monitor | 5 | 6200 |
| 1009 | Acer 24 Inch LED Monitor | 5 | 8000 |
| 1010 | SanDisk Ultra 32GB USB | 10 | 550 |

  
**EXERCISES**

1.  Add all quantity with 2 for all the products.
2.  Subtract 200 from quantity for products greater than 3000.
3.  Increase the price by 5% for all the products whose quantity less than 5.

## **PRODUCTS TABLE – CREATE QUERY**
``` sql
CREATE TABLE IF NOT EXISTS products(
    productid INT UNSIGNED AUTO_INCREMENT,
    description VARCHAR(30) DEFAULT '',
    quantity INT UNSIGNED DEFAULT 0,
    price DECIMAL(7,2) DEFAULT 99999.99,
    PRIMARY KEY (productid)
);
```

### **Insert into PRODUCTS Table**

(Productid is AUTO_INCREMENT, so no need to insert it)
```sql
INSERT INTO products 
    (description, quantity, price)
VALUES 
    ('4GB DDR4 RAM', 5, 1100), 
    ('ASUS M5A78L-M Motherboard', 2, 9852),
    ('Gigabyte N3050M Motherboard', 5, 4890),
    ('Gigabyte 78LMT Motherboard', 2, 6800),
    ('Dell 21.5 Inch LED Monitor', 5, 6200),
    ('Acer 24 Inch LED Monitor', 5, 8000),
    ('SanDisk Ultra 32GB USB', 10, 550);
```

### **Select all products**
```sql

SELECT * FROM products;
```

### **Select products where price > 3000**
```sql

SELECT * FROM products WHERE price > 3000;
```

### **Select products where quantity < 5**
```sql 
SELECT * FROM products WHERE quantity < 5;
```

### Exercise 1
Add 2 to quantity for all products.
```sql 
UPDATE products
SET quantity = quantity + 2;
```

### Exercise 2
Subtract 200 from quantity for products greater than 3000. (Here logically it should be price > 3000.)
```sql 
UPDATE products
SET quantity = quantity - 200
WHERE price > 3000;
```

### Exercise 3
Increase price by 5% for products whose quantity < 5.
```sql 
UPDATE products
SET price = price + (price * 0.05)
WHERE quantity < 5;
```
OR
```sql 
UPDATE products
SET price = price * 1.05
WHERE quantity < 5;
```