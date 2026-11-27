# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
<img width="675" height="312" alt="image" src="https://github.com/user-attachments/assets/b69b7d68-fe7d-4a2c-a515-8681ef47cdae" />


```sql
select gender,count(*) as TotalPatients
from patients
group by gender;
```

**Output:**

<img width="413" height="222" alt="image" src="https://github.com/user-attachments/assets/62957172-dda9-4563-aee1-2f2d4532ffa0" />


**Question 2**
---
<img width="703" height="443" alt="image" src="https://github.com/user-attachments/assets/59fb2b4d-2bbc-43ca-a37e-52c370e16f50" />


```sql
select doctorid,count(*) as TotalPrescriptions
from prescriptions
group by doctorid;
```

**Output:**

<img width="487" height="488" alt="image" src="https://github.com/user-attachments/assets/f5dfab32-8d0f-401f-a5ae-d987f86bde60" />


**Question 3**
---
<img width="696" height="426" alt="image" src="https://github.com/user-attachments/assets/397135d9-9083-40cc-951b-f045094490f6" />


```sql
select patientid,count(*) as TotalMedications
from prescriptions
group by patientid;
```

**Output:**

<img width="507" height="488" alt="image" src="https://github.com/user-attachments/assets/635460c5-7725-40cd-a06b-39ad245855c2" />


**Question 4**
---
<img width="597" height="317" alt="image" src="https://github.com/user-attachments/assets/007f615c-49e9-493b-99ae-b654abc59207" />


```sql
SELECT NAME,MAX(INCOME) AS 'max(income)'
from employee
where city='California'
```

**Output:**

<img width="392" height="188" alt="image" src="https://github.com/user-attachments/assets/d3d11fd9-b2e4-4d2d-a0b9-bc28862ce978" />


**Question 5**
---
<img width="687" height="302" alt="image" src="https://github.com/user-attachments/assets/85d1b55a-af60-4230-97ba-5cd22468f862" />


```sql
SELECT 
    AVG(LENGTH(email)) AS avg_email_length_below_30
FROM 
    customer
WHERE 
    city = 'Mumbai';
```

**Output:**

<img width="448" height="190" alt="image" src="https://github.com/user-attachments/assets/c97556cb-a027-43d5-a036-6ed8672f8cad" />


**Question 6**
---
<img width="860" height="312" alt="image" src="https://github.com/user-attachments/assets/c26179b1-64eb-4b7e-9b88-669f4b7cf19b" />


```sql
select count(*) AS 'COUNT'
from employee
where age > 32;
```

**Output:**

<img width="280" height="192" alt="image" src="https://github.com/user-attachments/assets/79ff5fc3-30c6-461b-8219-cc4945d46f44" />


**Question 7**
---
<img width="452" height="337" alt="image" src="https://github.com/user-attachments/assets/4df3afa8-3c4b-4611-bad5-c5433092f2c5" />


```sql
SELECT AVG(income) AS Average_Salary
FROM employee;
```

**Output:**


**Question 8**
---
<img width="1262" height="312" alt="image" src="https://github.com/user-attachments/assets/2adb9a21-859c-4b72-a083-d3943b891434" />


```sql
SELECT
    jdate,
    MAX(workhour)
FROM
    employee1
GROUP BY
    jdate
HAVING
    MAX(workhour) > 12;
```

**Output:**

<img width="412" height="247" alt="image" src="https://github.com/user-attachments/assets/e53bab1b-ac22-4896-a804-25aef63f1e3c" />


**Question 9**
---
<img width="1307" height="305" alt="image" src="https://github.com/user-attachments/assets/be8baa7d-6cfe-4808-95a2-c5288c487fdc" />


```sql
select occupation,avg(workhour) as 'AVG(workhour)'
from employee1
group by occupation
having AVG(workhour) between 10 and 12;
```

**Output:**

<img width="432" height="236" alt="image" src="https://github.com/user-attachments/assets/e59266f0-2442-40c7-9813-06c667d5383a" />


**Question 10**
---
<img width="1272" height="317" alt="image" src="https://github.com/user-attachments/assets/2243c30b-3805-4ce6-b7a0-a44ecbac9780" />


```sql
SELECT 
    p.category_id,
    p.product_name,
    p.Price AS Price
FROM 
    products p
WHERE 
    p.Price = (
        SELECT MAX(Price)
        FROM products
        WHERE category_id = p.category_id
    )
AND 
    p.Price > 15;
```

**Output:**

<img width="618" height="252" alt="image" src="https://github.com/user-attachments/assets/6aef456c-9154-463f-a921-fbef35f0b4c8" />



## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
