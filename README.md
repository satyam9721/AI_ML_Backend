setup;-

mkdir ai-ml-backend

cd ai-ml-backend

Create virtual environment

> python3 -m venv venv

activate it:

> source venv/bin/activate

Install required libraries

Create requirements.txt.

> pip install -r requirements.txt

Understanding the architecture

Important: Keep CRUD operations separate from business logic.

For example:

- crud/ml_model.py → Database queries.
- services/ml_service.py → Load, train, predict, evaluate ML models.
- api/v1/endpoints/ml_models.py → HTTP endpoints.

This separation makes the application easier to maintain.

---

How they communicate

                 FASTAPI
                    |
          +---------+---------+
          |         |         |
      PostgreSQL  Redis    SlowAPI
          |         |
       Alembic    Celery
                    |
               Background
                 Workers

              FASTAPI /metrics
                    |
                PROMETHEUS
                    |
                 GRAFANA
                    |
               DASHBOARDS

name of file -> work
of file

main.py

Main application entry point

api/

API routing and dependencies

api/v1/

Version 1 API routes

core/

Configuration and application settings

db/

Database connection and configuration

models/

SQLAlchemy database models

schemas/

Pydantic request/response schemas

crud/

Create, Read, Update, Delete operations

services/

Business logic and AI/ML processing

migrations/

Database schema migrations

tests/

Automated testing
