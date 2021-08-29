### containerize-PHP-and-Apache

A example of containerize PHP and Apache in localhost.

### How it works

1. Refresh the web page after editing the files inside the folder `public_html`. Files will be auto synced.
2. Modify the config in side the `.env` file, default:

```
PHP_VERSION=7.3
APACHE_VERSION=2.4.32
APACHE_PORT=4000
PROJECT_ROOT=./public_html
```

### How to run

1. Download the docker desktop - `https://www.docker.com/products/docker-desktop`
2. CD to the folder via `CMD`
3. Type `docker-compose up` -> will brings up all the services: `apache`, `php`
4. Open web browser and type `localhost:4000` and the message will showed

```
Hello World!
Testing php message!
```

You should see below messages if everything goes well.

```
php       | [29-Aug-2021 06:33:47] NOTICE: fpm is running, pid 1
php       | [29-Aug-2021 06:33:47] NOTICE: ready to handle connections
apache    | [Sun Aug 29 06:33:47.758447 2021] [mpm_event:notice] [pid 1:tid 139668005006152] AH00489: Apache/2.4.32 (Unix) configured -- resuming normal operations
apache    | [Sun Aug 29 06:33:47.758537 2021] [core:notice] [pid 1:tid 139668005006152] AH00094: Command line: 'httpd -D FOREGROUND'
```

### Helpers

1. If the html files not update, run the command below to stop the container servers.

```
docker-compose down
```

2. And start the container servers again with

```
docker-compose up
```

### Thanks to

https://github.com/mzazon/php-apache-mysql-containerized
