# Kittygram - социальная сеть для владельцев котиков

[![Django](https://img.shields.io/badge/Django-4.2-green.svg)](https://www.djangoproject.com/)
[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![Docker](https://img.shields.io/badge/Docker-✓-blue.svg)](https://www.docker.com/)

Социальная платформа для владельцев кошек, где можно делиться фотографиями и достижениями своих питомцев, а также знакомиться с другими котиками.

## Возможности

### Основной функционал
- Публикация фотографий и описания котиков
- Просмотр информации о других котиках
- Система достижений для питомцев

### Профили котиков
- Детальная информация о каждом котике
- Указание имени, цвета и даты рождения
- Система достижений для питомцев
  

## Технологический стек

- Django - Веб-фреймворк
- Python - Основной язык программирования
- Gunicorn - WSGI-сервер
- Nginx - Веб-сервер
- Docker - Контейнеризация приложения
- PostgreSQL - База данных

## Быстрый старт

### Предварительные требования
- Docker и Docker Compose
- Python 3.9 или новее

### Установка и запуск

1. Клонируйте репозиторий:
```bash
git clone https://github.com/daniltivodar/drf_docker_kittygram.git
cd kittygram
```

2. Настройте окружение:
Создайте файл .env со следующим содержимым:
```bash
SECRET_KEY='your-secret-key-here'
POSTGRES_USER=username
POSTGRES_PASSWORD=password
DB_HOST=db
DB_PORT=5432
ALLOWED_HOSTS=localhost,127.0.0.1
```

3. Запустите сервисы:
```bash
docker compose pull
docker compose up -d
```

4. Примените миграции базы данных:
```bash
docker compose exec backend python manage.py migrate
```

5. Соберите статические файлы:
```bash
docker compose exec backend python manage.py collectstatic
```

## Разработчик

**Данил Тиводар**  
[GitHub Профиль](https://github.com/daniltivodar)
