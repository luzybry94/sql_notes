# SQL Cheat Sheet

<h5>Database Basics</h5>

<li>Create Database</li>

```
sqlite3 pets_database.db
```

<li>Create Table</li>

```
CREATE TABLE cats (
id INTEGER PRIMARY KEY,
name TEXT, 
age INTEGER
);
```

<li>Alter Table</li>

```
ALTER TABLE cats ADD COLUMN breed TEXT;
```

<li>Delete Table</li>

```
DROP TABLE cats;
```

<h5>Inserting, Updating, and Selecting</h5>

<li>Add to Table</li>

```
INSERT INTO cats (name, age, breed) VALUES ('Maru', 3, 'Scottish Fold');
```

<li>Add to Table via Code Editor</li>

```
sqlite3 pets_database.db < 01_insert_cats_into_cats_table.sql
```

<li>Select Specific Data from Table</li>

```
SELECT id, name, age, breed FROM cats;
```

<li>Select All Data from Table</li>

```
SELECT * FROM cats;
```

<li>Select Unique Data</li>

```
SELECT DISTINCT name FROM cats;
```

<li>Selecting Based on Conditions</li>

```
SELECT * FROM cats WHERE age < 2;
```

<li>Updating Data</li>

```
UPDATE cats SET name = "Hana" WHERE name = "Hannah";
```

<li>Deleting Data</li>

```
DELETE FROM cats WHERE id = 2;
```


<h5>Query Modifiers</h5>

<li>Order By</li>

```
SELECT * FROM cats ORDER BY age DESC;
```

<li>Limit</li>

```
SELECT * FROM cats ORDER BY age DESC LIMIT 2;
```

<li>Between</li>

```
SELECT name FROM cats WHERE age BETWEEN 1 AND 3;
```

<h5>Aggreagate Functions</h5>

<li>Count</li>

```
SELECT COUNT(owner_id) FROM cats WHERE owner_id = 1;
```

<li>Group By</li>

```
SELECT breed, owner_id, COUNT(breed) FROM cats GROUP BY breed, owner_id;
```

<li>Average (with alias)</li>

```
SELECT AVG(net_worth) AS average_net_worth FROM cats;
```

<li>Sum</li>

```
SELECT SUM(net_worth) FROM cats;
```

<li>Min/Max</li>

```
SELECT MIN(net_worth) FROM cats;
```




















 




















<b>Helpful SQL Interface Commands:</b>

`.schema` - see table schema
`.quit` - quit SQL interface
`.tables` - see all table in current database
`.help` - see all SQL commands
`.headers on` - output the name of each column
`.mode column` - enable column mode
`.width auto` - adjusts and normalizes column width
`.width NUM1, NUM2` - customize column width


