sandbox-docker-phpinfo-apache
======

## Compose

```
$ docker-compose up -d
```

And browse by HTTP.


## php-fpm

```
$ docker build -t sandbox-phpinfo-phpfpm ./phpfpm
$ docker run --name phpfpm -d sandbox-phpinfo-phpfpm
```

## nginx

```
$ docker build -t sandbox-phpinfo-nginx ./nginx
$ docker run --name nginx -p 80:80 --link phpfpm:php -d sandbox-phpinfo-nginx
```
