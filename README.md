# AM Cinema

A cinema website built on WordPress and Elementor, running as a Docker Compose stack that starts with a single command.

**Stack:** Docker Compose · WordPress · MySQL 8 · phpMyAdmin

## Services

| Service | Port | Role |
|---|---|---|
| `wordpress` | 8080 | The site |
| `mysql` | 3306 | Database, with a health check |
| `phpmyadmin` | 8081 | Database admin UI |

## Setup

- **Private network:** the services reach each other by name
- **Persistent volume:** data survives restarts and rebuilds
- **Auto-seeding:** `baza.sql` loads the full site into a fresh database
- **Health check and auto-restart** on MySQL
- **Config in env files**, not in the compose file

## Run

```bash
docker compose up -d
```

Site: http://localhost:8080 · phpMyAdmin: http://localhost:8081
