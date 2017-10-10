# Microservices

Сборка образа:

``` sh
$ docker build -t reddit:latest github.com/7even/microservices
```

Запуск:

``` sh
$ docker run --name reddit -d --network=host reddit:latest
```

Остановка:

``` sh
$ docker stop reddit
```
