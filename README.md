# Microservices

Сборка образа:

``` sh
$ docker build -t <your-login>/post:1.0 ./post-py
$ docker build -t <your-login>/comment:1.0 ./comment
$ docker build -t <your-login>/ui:2.0 ./ui
```

Запуск:

``` sh
$ docker run -d --network=reddit \
  --network-alias=post_db --network-alias=comment_db mongo:latest

$ docker run -d --network=reddit \
  --network-alias=post <your-login>/post:1.0

$ docker run -d --network=reddit \
  --network-alias=comment <your-login>/comment:1.0

$ docker run -d --network=reddit \
  -p 9292:9292 <your-login>/ui:2.0
```

Остановка:

``` sh
$ docker kill $(docker ps -q)
```
