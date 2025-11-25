# CRM Project Backend

This directory contains a production-ready Django CRM backend scaffold featuring JWT authentication, DRF APIs, Celery tasks, Redis-backed channels, and a default SQLite configuration. It is intended to pair with a React/Vue frontend.

## Key features
- Django 4.2 with Django REST Framework and Simple JWT
- Custom user model with role-based access control
- Contacts, companies, deals, and activities with filtering and pagination
- Swagger docs powered by drf-spectacular
- WebSocket notifications using Django Channels and Redis
- Celery setup for background jobs
- AWS S3-ready file storage via `django-storages`
- Docker targets for backend, frontend, Redis, and PostgreSQL

## Getting started
1. Create a virtual environment and install `backend/requirements.txt`.
2. Set required environment variables (database credentials, AWS keys, CORS origins).
3. Run migrations: `python manage.py migrate`.
4. Start supporting services (Redis for channels/Celery if you need them) and run `python manage.py runserver`.

## Running locally with SQLite
1. `cd backend`
2. Create and activate a virtual environment: `python -m venv .venv && source .venv/bin/activate`
3. Install dependencies: `pip install -r requirements.txt`
4. Copy `.env` and set any desired Django settings (e.g., `DJANGO_SECRET_KEY`, `DJANGO_DEBUG`).
5. Run database migrations: `python manage.py migrate`
6. Start the server: `python manage.py runserver`

SQLite stores data in `backend/db.sqlite3` by default, so no external database service is required.
