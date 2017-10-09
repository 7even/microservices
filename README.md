# Microservices

Сборка образа:

``` sh
$ docker build -t reddit:latest .
```

Запуск:

``` sh
$ docker run --name reddit -d --network=host reddit:latest
```

Остановка:

``` sh
$ docker stop reddit
```
