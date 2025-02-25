# Завдання 1: Відображення таблиці order_details з customer_id

## Опис
Напишіть SQL-запит, який відображає всі записи з таблиці `order_details` та додає поле `customer_id` з таблиці `orders` відповідно для кожного запису.  
Це має бути зроблено за допомогою вкладеного запиту в операторі `SELECT`.

## SQL-запит
```sql
SELECT 
    od.*, 
    (SELECT o.customer_id FROM orders o WHERE o.id = od.order_id) AS customer_id
FROM 
    order_details od;

![Результат запиту](images/1.png)
