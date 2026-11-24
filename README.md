Understanding the architecture

Important: Keep CRUD operations separate from business logic.

For example:

- crud/ml_model.py → Database queries.
- services/ml_service.py → Load, train, predict, evaluate ML models.
- api/v1/endpoints/ml_models.py → HTTP endpoints.

This separation makes the application easier to maintain.

---

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
