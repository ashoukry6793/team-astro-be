# Team Astro Backend

Backend API built with NestJS, TypeORM, and PostgreSQL.

## Quick Start

### 1. Start PostgreSQL with Docker

```bash
docker run -d \
  --name team-astro-db \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=postgres \
  -e POSTGRES_DB=app \
  -p 5432:5432 \
  postgres:16-alpine
```

### 2. Set up environment

```bash
cp .env.example .env
```

The default `.env` values match the Docker container above — no changes needed.

### 3. Install dependencies and run

```bash
npm install
npm run start:dev
```

The server will start on `http://localhost:3000`. TypeORM will auto-sync the schema in development.

### 4. Verify

```bash
curl http://localhost:3000
# => Hello World!
```

### Useful Docker commands

```bash
# Stop the database
docker stop team-astro-db

# Start it again
docker start team-astro-db

# Remove the container (data will be lost)
docker rm -f team-astro-db

# View logs
docker logs team-astro-db
```

## Scripts

| Command | Description |
|---------|-------------|
| `npm run start:dev` | Start in watch mode |
| `npm run start:debug` | Start in debug mode |
| `npm run build` | Build for production |
| `npm run start:prod` | Run production build |
| `npm test` | Run unit tests |
| `npm run test:e2e` | Run e2e tests |
| `npm run lint` | Lint and fix |

## Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `DB_HOST` | `localhost` | PostgreSQL host |
| `DB_PORT` | `5432` | PostgreSQL port |
| `DB_USERNAME` | `postgres` | Database username |
| `DB_PASSWORD` | `postgres` | Database password |
| `DB_NAME` | `app` | Database name |
| `PORT` | `3000` | Server port |
