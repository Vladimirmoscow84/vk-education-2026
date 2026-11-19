# Отчет по лекции 2 

1. Сервис: `db`, статус `Up (healthy)` — `docker compose ps`.
2. Образ: `postgres:16.4` (тег зафиксирован, `latest` не используется) — `docker compose images`.
3. Том: `postgres_data` примонтирован в `/var/lib/postgresql/data` — `docker volume ls`, `docker inspect`.
4. Состояние: `running`, health `healthy` — `docker inspect vk_course_db`.
5. Адрес/порт: `127.0.0.1:55432 -> 5432/tcp` (публикация только на localhost) — `docker compose port db 5432`.
6. Ответ на запрос: `PostgreSQL 16.4 ... (1 row)` — `psql -c "SELECT version();"`.
7. Внутренний порт: `5432` (не менялся).
8. Внешний порт: `55432` (из `POSTGRES_PORT` в `.env`).
9. Имя сервиса: `db` (строчными буквами).
10. Имя тома: `postgres_data`.
11. Данные: только синтетические, реальные резюме не используются.
