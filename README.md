# Commands



## Docker setup

> If you have native PostgreSQL instances installed on Windows (which typically occupy ports 5432 and 5433), map the Docker container to port `5434` to avoid conflicts.

```bash
docker run --name lavapro-db -p 5432:5432 -e POSTGRES_USER=lavapro -e POSTGRES_PASSWORD=lavapropass!123 -e POSTGRES_DB=lavapro_api -d postgres
```

## Docker compose
```docker-compose up -d```

```python
SQLALCHEMY_DATABASE_URL = "postgresql://lavapro:lavapropass!123@localhost:5432/lavapro_api"
```

## Create VENV
```uv venv```

## Activate VENV:
Windows: ```.venv\Scripts\activate```
Linux: ```source .venv/bin/activate```

## Run fastapi server:
```uv run fastapi dev app/main.py```