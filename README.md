# Домашнее задание к занятию "`Работа с данными (DDL/DML)`" - `Дёмин Максим`


### Задание 1

Что нужно сделать:

1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

1.2. Создайте учётную запись sys_temp.

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

1.4. Дайте все права для пользователя sys_temp.

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

1.6. Переподключитесь к базе данных от имени sys_temp.

Для смены типа аутентификации с sha2 используйте запрос:
```
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.

### Решение:

1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.
```
docker exec -it mysql8 mysql -u sys_temp -p
```
<img width="1479" height="418" alt="image_2026-02-25_22-09-14" src="https://github.com/user-attachments/assets/b22f1bd3-b891-45b5-9a3e-5e9402896920" />

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)
<img width="609" height="328" alt="image_2026-02-25_22-08-24" src="https://github.com/user-attachments/assets/83b25335-7feb-4b8f-8391-693b234c4c88" />

1.2. Создайте учётную запись sys_temp.
<img width="698" height="68" alt="image_2026-02-25_22-09-44" src="https://github.com/user-attachments/assets/89860efb-528c-4279-86c0-750d9062047a" />

1.4. Дайте все права для пользователя sys_temp.
<img width="793" height="135" alt="image_2026-02-25_22-10-53" src="https://github.com/user-attachments/assets/bb429192-35dd-4599-ab8f-ba5a1966a8db" />

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)
<img width="1919" height="736" alt="image_2026-02-25_22-12-08" src="https://github.com/user-attachments/assets/29b1cd88-6364-4885-bddf-408432c8d16a" />

1.6. Переподключитесь к базе данных от имени sys_temp.

Для смены типа аутентификации с sha2 используйте запрос:
```
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.
<img width="799" height="666" alt="image_2026-02-25_22-19-15" src="https://github.com/user-attachments/assets/586f7836-4993-4d45-a308-e311a9315303" />
```
wget https://downloads.mysql.com/docs/sakila-db.zip
unzip sakila-db.zip
docker cp sakila-db/sakila-schema.sql mysql8:/tmp/sakila-schema.sql
docker cp sakila-db/sakila-data.sql mysql8:/tmp/sakila-data.sql
docker cp sakila-db/sakila.mwb mysql8:/tmp/sakila.nwb
```
1.7. Восстановите дамп в базу данных.
<img width="508" height="917" alt="image_2026-02-25_22-35-15" src="https://github.com/user-attachments/assets/bb80721e-6b62-4e3f-8834-142013e2f311" />

<img width="508" height="917" alt="image_2026-02-25_22-35-34" src="https://github.com/user-attachments/assets/17bbe41d-3a7a-44f1-be87-448e0f3f3876" />

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)
<img width="416" height="743" alt="image_2026-02-25_22-35-51" src="https://github.com/user-attachments/assets/5943a5ba-5488-489d-aad3-88295bca931a" />

