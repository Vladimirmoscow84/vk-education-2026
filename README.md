# VK Education 2026 — Course Project (Go)

Учебный проект курса VK Education. Репозиторий содержит окружение для запуска
сервиса базы данных PostgreSQL 16.4. Бэкенд будет написан на Go (см. `backend/`).

## Требования
- Git
- Docker Desktop (Docker 28+, Compose v2)
- macOS / Linux / Windows (WSL2)

## Быстрый старт
1. Клонировать репозиторий:
   git clone <repo-url>
   cd vk-education-2026

2. Создать локальные настройки:
    cp .env.example .env

3. Поднять БД:
    docker compose up -d

4. Дождаться статуса healthy:
    docker compose ps

## Проверка
    docker compose ps
    docker compose images
    docker volume ls | grep postgres_data
    docker compose exec db psql -U course_user -d course_db -c "SELECT version();"
    docker compose port db 5432

## Структура репозитория
    
├── compose.yaml       # описание сервиса db
├── .env.example       # шаблон переменных окружения
├── .env               # локальные настройки (НЕ коммитится)
├── .gitignore
├── README.md
├── backend/           # Go-сервис
├── db/                # материалы по базе данных
└── docs/              # документация

## Данные
В проекте используются только синтетические данные. Реальные резюме,
персональные данные, логи и скриншоты в репозиторий не помещаются.

## "Проврено на чистой копии"
