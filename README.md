# SQL

##Задача 1

![image](https://github.com/user-attachments/assets/4a06a8aa-d990-407b-a004-8068d52b1e79)

```
SELECT name
FROM county as co
LEFT JOIN customer as c on co.county_code=c.county_code
LEFT JOIN c_orders as c_ord on c.id_customer=c_ord.id_customer
WHERE c_ord.id_orders ISNULL

```

![image](https://github.com/user-attachments/assets/6a52222e-e93d-42e2-9448-2881333b184a)
