```bash
# Log in to PostgreSQL using username
psql -h localhost -U your_username -d your_database_name
```

```sql
-- View all tables
\dt;
```

```sql
-- See data from a particular table (e.g., products)
SELECT * FROM products;
```

```sql
-- Update a table (e.g., update sales_volume in sales_data where id is 1)
UPDATE sales_data
SET sales_volume = 5
WHERE id = 1;
```

```sql
-- Get products where category is 'phone'
SELECT * FROM products
WHERE category = 'phone';
```

```sql
-- Insert into a table (e.g., insert one record into sales_data)
INSERT INTO sales_data (product_id, sales_volume, date)
VALUES (1, 10, '2024-10-01');
```

```sql
-- Insert into a table (e.g., insert two records into sales_data)
INSERT INTO sales_data (product_id, sales_volume, date)
VALUES 
    (2, 15, '2024-10-02'),
    (3, 20, '2024-10-03');
```

### Example Output (products table):
| id  | name            | category | price | rating |
|-----|-----------------|----------|-------|--------|
| 5   | iphone14        | phone    | 850   | 4.7    |
| 6   | samsung galaxy  | phone    | 900   | 4.5    |
| 12  | google pixel 7  | phone    | 700   | 3.1    |

### Example Output (sales_data table after insert):
| id  | product_id | sales_volume | date       |
|-----|------------|--------------|------------|
| 1   | 1          | 10           | 2024-10-01 |
| 2   | 2          | 15           | 2024-10-02 |
| 3   | 3          | 20           | 2024-10-03 |
