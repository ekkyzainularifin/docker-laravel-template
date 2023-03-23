
# Boiler Plate for docker laravel


## Installation

After you clone this repository, you need follow installation step bellow

```bash
  cd BOILERPLATE_DOCKER_LARAVEL
  mkdir src
  cd src/
```

install or clone your laravel project inside src folder you have created before, and create .env file.

after that you need set permission storage folder, follow steps bellow to set permission

```bash
sudo chgrp -R 82 storage/
sudo chmod -R ug+rwx storage/
```
## Running
When you finish installation steps, you need back to boilerplate root folder, then up & build docker compose with command bellow

```bash
  docker compose -p PROJECT_NAME up -d --build
```

after run docker compose command you need to check container, and copy container ID / Name, and you must run `composer install` first inside container, use command bellow to `composer install`

```bash
docker exec -it CONTAINER_NAME composer install
docker exec -it CONTAINER_NAME php artisan key:generate
```
