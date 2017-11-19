# Microservices

Сборка образов и запуск:

``` sh
$ cp .env.example .env
$ emacs .env # подставить свой юзернейм в первой строке
$ docker-compose up -d
```

Приложение будет доступно на `9292` порту.

Остановка:

``` sh
$ docker-compose down
```

Запуск в Docker Swarm:

``` sh
$ docker stack deploy --compose-file=<(docker-compose -f docker-compose.infra.yml -f docker-compose.yml config 2>/dev/null) DEV
```
