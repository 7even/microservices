# Microservices

## Сборка образов и запуск локально:

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

## Запуск в Docker Swarm:

Для запуска в Swarm должна быть нода с лейблом `reliability = high`. Установить этот лейбл можно следующим образом:

``` sh
$ docker node update --label-add reliability=high master-1
```

(где `master-1` - имя ноды)

Запуск приложения выполняется следующей командой:

``` sh
$ docker stack deploy --compose-file=<(docker-compose -f docker-compose.infra.yml -f docker-compose.yml config 2>/dev/null) DEV
```
