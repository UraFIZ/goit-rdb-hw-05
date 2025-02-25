# Завдання 2: Фільтрація order_details за shipper_id

## Опис
Напишіть SQL-запит, який відображає всі записи з таблиці `order_details`,  
але тільки для тих записів, де відповідне замовлення (`orders`) має `shipper_id = 3`.  
Це має бути зроблено за допомогою вкладеного запиту в операторі `WHERE`.

## SQL-запит
```sql
SELECT * 
FROM order_details 
WHERE order_id IN (
    SELECT id FROM orders WHERE shipper_id = 3
);
```
![Результат запиту](images/2.png)