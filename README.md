<div align="center">
    <img src="https://res.cloudinary.com/rexcuni/image/upload/v1688969225/favicon_oxddqi.png" width="80px">
    <br>
    <h1>Docker WordPress</h1>
</div>
<p align="center">
    <a href="https://didepanlayar.com" target="_blank"><img alt="" src="https://img.shields.io/badge/Website-1DA1F2?style=normal&logo=dribbble&logoColor=white" style="vertical-align: center" /></a>
    <a href="https://instagram.com/didepanlayar" target="_blank"><img alt="" src="https://img.shields.io/badge/Instagram-DD2A7B?style=normal&logo=instagram&logoColor=white" style="vertical-align: center" /></a>
    <a href="https://www.youtube.com/@didepanlayar" target="_blank"><img alt="" src="https://img.shields.io/badge/YouTube-CD201F?style=normal&logo=youtube&logoColor=white" style="vertical-align: center" /></a>
</p>

## Description
WordPress Themes and Plugins Development using Docker.

## Install Prerequisites
All requisites should be available for your distribution. The most important are:
1. [Git](https://git-scm.com/downloads)
2. [Docker](https://docs.docker.com/engine/installation)
3. [Docker Compose](https://docs.docker.com/compose/install)

## Overview
All images are used:
| Name                                            | Tag        |
| ----------------------------------------------- | ---------- |
| [WordPress](https://hub.docker.com/_/wordpress) | php7.4-fpm |
| [Nginx](https://hub.docker.com/_/nginx/)        | 1.25.2     |
| [MariaDB](https://hub.docker.com/_/mariadb)     | 10.11.5    |

## Project Tree

```sh
.
├── Makefile
├── README.md
├── data
├── docker-compose.yml
├── logs
│   └── nginx
├── nginx
│   └── sites
│       └── default.conf
├── php-fpm
│   └── php.ini
└── src
    ├── plugins
    │   └── index.php
    ├── themes
    │   └── index.php
    └── uploads
```

## Environment
To run this project you need to add following environment variables to your `.env` file.

```
# Application
APP_NAME=myapp

# WordPress
WORDPRESS_DB_NAME=db_wordpress
WORDPRESS_TABLE_PREFIX=wp_

# MariaDB
MARIADB_USER=default
MARIADB_PASSWORD=secret
MARIADB_ROOT_PASSWORD=root
```

## Run
1. Copy and modify the `.env` file.

    ```sh
    cp .env.example .env
    ```

    Modify the `.env` file with the following [Environment](#environment) above.

2. Start services.

    ```sh
    docker-compose up -d
    ```

3. Stop and clear services.

    ```sh
    docker-compose down -v
    ```

Or, you can use a Makefile to run the service.

```sh
make help
```

## Tech Stack
- Git
- Docker
- Docker Compose
- Visual Studio Code
- DBeaver
