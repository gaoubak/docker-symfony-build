
# Symfony 6 + PHP 8.0.13 with Docker

**ONLY for DEV, not for production**

A very simple Docker-compose to discover Symfony 5 with PHP 8.0.13 in 5 minutes
## Run Locally

Clone the project

```bash
 git@github.com:gaoubak/docker-symfony-build.git
```

Run the docker-compose

```bash
  docker compose build --no-cache --pull
  docker-compose up -d
```

Log into the PHP container

```bash
  docker exec -it  nom-du-container bash
```

Create your Symfony application and launch the internal server

```bash
  symfony new new-project --full
  cd new-project
  symfony serve -d
```

If you need a database, create a file .env.local file like this example:

```yaml
 DATABASE_URL="mysql://app:!ChangeMe!@127.0.0.1:3306/app?serverVersion=8&charset=utf8mb4"
```

## Ready to use with

This docker-compose provides you :

- PHP-8.0.13-cli (Debian)
    - Composer
    - Symfony CLI
    - pdo pdo_mysql pdo_pgsql opcache intl zip calendar dom mbstring gd xsl
    - nodejs, npm, yarn
- mailcatcher


## Requirements

Out of the box, this docker-compose is designed for a Linux operating system, provide adaptations for a Mac or Windows environment.

- Linux (Ubuntu 20.04 or other)
- Docker
- Docker-compose
