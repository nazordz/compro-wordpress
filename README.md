# Containerized Wordpress COMPRO

## Starting for first time
When a container is started for the first time, a new database with the specified name will be created and initialized with the provided configuration variables. Furthermore, it will execute files with extensions .sh, .sql and .sql.gz that are found in `/docker-entrypoint-initdb.d`. Files will be executed in alphabetical order

## Migration
[Migration guide is here!](https://www.wpbeginner.com/wp-tutorials/how-to-move-wordpress-from-local-server-to-live-site/#manual-method-local-to-live)

### Run in local for development environment
```bash
docker compose -f docker-compose.dev.yml up -d
```

### Run in local for production environment
```bash
docker compose -f docker-compose.yml up -d --build
```

### Build image
```bash
docker build -t wp-compro .
```

### Run image build
```bash
docker compose -f docker-compose.yml up -d
```
