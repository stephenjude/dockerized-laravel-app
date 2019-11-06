## Dockerized Laravel App
A sample dockerized laravel app. 

## Usage

Make sure you have docker and docker compose on your machine.

[How To Install and Use Docker on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04)

[How To Install Docker Compose on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-install-docker-compose-on-ubuntu-18-04)

Clone the project

`cd` into the project directory

Run `docker-compose up -d`

This will build three docker container

app, db, webserver

Generate app key

```
docker-compose exec app php artisan key:generate
```

Cache configurations
```
docker-compose exec app php artisan config:cache
```

Enter the database and login to mysql
```
docker-compose exec db bash

mysql -u root -p
```
make use of the password defined inside the `docker-compose.yml` file.

