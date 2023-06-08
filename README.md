# DB_SQL_Yandex_Samokat

Первый запрос объединяет таблицы "Couriers" и "Orders" на основе полей "id" и "courierId" соответственно. 
Затем он фильтрует строки на основе условия o."inDelivery" = TRUE и группирует результат по логину курьера (c.login). 
Количество заказов со статусом "В доставке" рассчитывается с помощью COUNT(o.*).

Второй запрос выбирает колонку "track" из таблицы "Orders" и использует оператор CASE, 
чтобы определить статус на основе заданных правил: 
Если поле "finished" имеет значение TRUE, ему присваивается статус 2. 
Если поле "cancelled" имеет значение TRUE, ему присваивается статус -1. 
Если поле "inDelivery" имеет значение TRUE, ему присваивается статус 1. 
Для всех остальных случаев присваивается статус 0.
