## Задача 1

![image](https://github.com/user-attachments/assets/4a06a8aa-d990-407b-a004-8068d52b1e79)

```
SELECT name
FROM county as co
LEFT JOIN customer as c on co.county_code=c.county_code
LEFT JOIN c_orders as c_ord on c.id_customer=c_ord.id_customer
WHERE c_ord.id_orders ISNULL

```

![image](https://github.com/user-attachments/assets/6a52222e-e93d-42e2-9448-2881333b184a)


## Задача 2

![image](https://github.com/user-attachments/assets/23b06d37-f269-4dca-9645-50d66c3bc466)

```

SELECT DISTINCT an_name, an_price FROM analysis
WHERE an_price<1000 AND
(an_name LIKE '%anti%' OR LOWER(an_name) LIKE '%кров%')
ORDER BY an_price DESC

```

![image](https://github.com/user-attachments/assets/0bd4ab9e-e274-4d9b-aa44-9aa3e6f4216d)


## Задача 3

Распарсить строку:

![image](https://github.com/user-attachments/assets/6a01dfbc-2271-4961-9c08-abe52b4f6869)

Решение:

```
select str_columns,
 substring(trim(str_columns),1,1) as id,
  trim(substring(trim(str_columns),3,8)) as first_name,
  trim(substring(trim(str_columns),12,13)) as last_name,
  substring(trim(right(str_columns,10)),1,2) as age,
  trim(right(str_columns,1)) as gender
from skill_fix

```
![image](https://github.com/user-attachments/assets/dfa151a0-993e-4919-b58f-02d44a348288)


## Задача 4

![image](https://github.com/user-attachments/assets/323f2fc9-7b13-4c96-b539-ebaf318595d5)

```
SELECT COUNT (*) as cnt_users FROM 
  (SELECT DISTINCT user_id FROM ozon.purchases 
   WHERE CAST(created_at AS date)='2023-10-01' AND sku_id = '2')
   as ttt

```
