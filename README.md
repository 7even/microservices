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
