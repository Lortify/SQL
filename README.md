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
