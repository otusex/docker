# Docker nginx + php74-fpm

Необходимо для работы:

```bash
docker --version
Docker version 1.13.1, build 0be3e21/1.13.1

docker-compose --version
docker-compose version 1.27.4, build 40524192

```

Также необходимо отелбчить selinux

Запускать
```bash

git clone git@github.com:otusex/docker.git

cd docker

docker-compose up -d --build
```

Файл docker-compose.yml - создает и запускает два сервиса: nginx + php74-fpm,
также создается сеть и bind mount

Директория nginx - содержит докер файл + конфиги nginx
Директория php-fpm - содержит докер файл + конфиги php74-fpm
