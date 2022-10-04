# cube-demo
Repository to stand up a clickhouse and cube js environment locally via docker for testing

## Prerequiste
- Docker Desktop
## Quickstart

Clone this repo
```bash
git clone https://github.com/wookiee89/cube-demo.git
```
Stand up Clickhouse & CubeJS

```bash
docker compose up -d
```
Log into Clickhouse CLI

```bash
docker-compose exec ch_server clickhouse-client --user demo --pasword '123456'
```

Ensure data is loaded

```pgsql
USE demo;

SELECT * FROM trips LIMIT 10;
```

Access CubeJS Playground go to [localhost:4000](http://localhost:4000/)