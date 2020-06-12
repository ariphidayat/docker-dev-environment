# MariaDB

## Installation

- Compose file

    ```yaml
    version: '3.5'

    services:
      mariadb:
        container_name: mariadb
        image: mariadb:10.4.13
        environment:
            MYSQL_ROOT_PASSWORD: rahasia
        ports: 
            - 3306:3306
        volumes: 
            - data:/var/lib/mysql

    volumes: 
        data:
    ```

- Run

    ```bash
    $ docker-compose up -d
    ```

- Run Command in a running container

    ```bash
    $ docker exec -it mariadb bash
    ```

- Run mysql cli

    ```bash
    # mysql -u root -p
    ```

    Or you can use:

    ```bash
    # mariadb -u root -p
    ```

- Down

    ```bash
    $ docker-compose down
    ```

## MariaDB Cheat Sheet

- Show Databases

    ```bash
    > show databases;
    ```

- Create Database

    ```bash
    > create database [database name];
    ```

- Use Database

    ```bash
    > use [database name];
    ```

- Show Table

    ```bash
    > show tables;
    ```