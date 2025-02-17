﻿# Planetarium-API project

DRF project for managing planetarium and watching shows

### How to run

1. Clone the Repository
```shell
git clone https://github.com/Postpostman/planetarium-api
```
If project is empty, you should checkout to develop branch:
    git checkout develop

2. Configure Environment Variables
```shell
cp .env.sample .env
```
Open the .env file and fill in all the required fields with the appropriate data.
3. Build and Run Docker Containers
```shell
docker-compose up --build
```

4. Apply Migrations
Run migrations to set up the database schema:
    docker exec -it <container_id> python manage.py migrate
5. Create a Superuser

List the running Docker containers to find the container_id of the web service:
```shell
docker ps
```
Access the running container with:
```shell
docker exec -it <container_id> sh
```
Inside the container, create a superuser by running:
```shell
python manage.py createsuperuser
```
6. Access the API
http://localhost:8000/api/planetarium/

## Features

* Manage Planetarium: Create, update, and delete planetarium shows, domes, themes, and reservations.
* Admin Panel: Advanced management through the Django admin interface.
* Caching: Optimize performance with a cache system for specific pages.
* API Documentation: Swagger UI available at /api/doc/swagger/.
* Authentication: User authentication and JWT-based authorization.
* CRUD Operations: Full support for create, read, update, and delete actions on all endpoints with validation.

## Technology used

* Django Rest Framework
* Docker
* PostgreSQL
* Redis
* Swagger
* JWT


## Author

GitHub: Postpostman
