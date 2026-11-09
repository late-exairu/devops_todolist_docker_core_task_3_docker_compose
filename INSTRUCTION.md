#### Port Configuration

The application inside container listens on port 8080 (0.0.0.0:8080).
Docker compose maps host's port 8080 to the container's internal port 8080 (8080:8080).

#### Data Persistence

The application runs database migrations (python manage.py migrate) during the container build process.
By default, SQLite database state created during runtime persists within the container filesystem unless removed.

To **pull (or build)** the image and **start** the app in the background:

```bash
docker compose up -d
```

To **stop** and **remove** containers

```bash
docker compose down
```

To inspect Django output, migration logs, or runtime errors:

```bash
docker compose logs -f
```

Inspect Container Status

```bash
docker compose ps
```

To access the application in a browser open [localhost:8080](http://localhost:8080/)
