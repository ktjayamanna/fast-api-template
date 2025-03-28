# FastAPI Project Template

## Overview
This repository serves as a template for building FastAPI projects with modern Python tools and best practices. It includes configurations and setups for Pydantic, MyPy, Docker Compose, Pytest, Alembic, and SQLAlchemy.

## Project Structure

```
assets/
    general_project_structure.txt
	sys.png
backend/
	alembic/
		env.py
		script.py.mako
		versions/
	bitly/
		configs/
			__init__.py
			app_configs.py
			constants.py
		db/
			__init__.py
			engine.py
			models.py
		server/
			__init__.py
			feature_1/
				__init__.py
				api.py
				models.py
			feature_2/
				__init__.py
				api.py
				models.py
			middleware/
				__init__.py
		utils/
			__init__.py
			logger.py
	requirements/
		default.txt
		dev.txt
	scripts/
		bash/
			rename_project.sh
		python/
	shared_configs/
		__init__.py
		configs.py
	tests/
		integration/
			test_placeholder.py
		unit/
			test_placeholder.py
deployment/
	docker_compose/
		docker-compose.yml
other/
```

### Key Directories and Files

- **backend/**: Contains the core application code.
  - **alembic/**: Database migration scripts.
  - **bitly/**: Main application logic.
    - **configs/**: Configuration files for the application.
    - **db/**: Database-related code, including models and engine setup.
    - **server/**: API endpoints and middleware.
    - **utils/**: Utility functions and helpers.
  - **requirements/**: Dependency files for different environments.
  - **shared_configs/**: Shared configuration files across services.
  - **tests/**: Unit and integration tests.

- **deployment/**: Deployment-related files, including Docker Compose configurations.

- **assets/**: Static assets like images and diagrams.

- **scripts/**: Scripts for automation and project management.

## Technologies Used

- **FastAPI**: Web framework for building APIs.
- **Pydantic**: Data validation and settings management.
- **PostgreSQL**: Relational database.
- **Docker Compose**: Container orchestration.
- **Alembic**: Database migrations.
- **SQLAlchemy**: ORM for database interactions.
- **Pytest**: Testing framework.
- **MyPy**: Static type checker for Python.

## Getting Started

### Prerequisites

- Docker and Docker Compose installed.
- Python 3.9 or higher.

### Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <project-name>
   ```

2. Build and start the services using Docker Compose:
   ```bash
   docker-compose up --build
   ```

3. Run database migrations:
   ```bash
   docker-compose exec web alembic upgrade head
   ```

4. Access the application at `http://localhost:8000`.

### Running Tests

Run the tests using Pytest:
```bash
pytest
```

### Type Checking

Run MyPy to check for type errors:
```bash
mypy .
```