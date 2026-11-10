# Docker Activity

This Compose project runs the Student Account application as a local development
stack. Run the commands below from the repository root.

## Services

| Service | Compose service | URL |
| --- | --- | --- |
| React/Vite | `react` | http://localhost:3000 |
| Node.js API | `nodejs` | http://localhost:3002 |
| Laravel/PHP | `laravel` | http://localhost:8080 |
| phpMyAdmin | `phpmyadmin` | http://localhost:8081 |
| MySQL | `mysql` | localhost:3306 |

## Start

From the repository root:

```powershell
docker compose up -d --build
```

Check service health:

```powershell
docker compose ps
docker compose logs -f nodejs laravel
```

Stop the stack without deleting database data:

```powershell
docker compose down
```

The source directories are mounted into the containers, so code changes remain
in the main project:

- `../frontend`
- `../api-server`
- `../backend`
