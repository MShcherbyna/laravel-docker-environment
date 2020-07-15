# Laravel dev environment (nginx, mysql, phpmyadmin, composer, npm)

## Getting Started

- Rename ".env.example" to ".env" and update the .env file along with database connection

```bash
mv .env.example .env
```

- Build docker containers

```bash
docker-compose up --build -d
```
- Install dependencies for app

```bash
docker-compose run --rm composer install && docker-compose run --rm composer update
docker-compose run --rm npm install
```

- Generate key

```bash
docker-compose run --rm artisan key:generate
```
- Create necessary tables

```bash
docker-compose run --rm artisan migrate
```

## Usage

After you run the project open in your browser:

- Start page: http://localhost:8088/
- Phpmyadmin: http://localhost:3888/

