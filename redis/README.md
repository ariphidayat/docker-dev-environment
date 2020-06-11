# Redis

- Compose file

    ```yaml
    version: '3.5'

    services:
      redis:
        container_name: redis
        image: redis:6.0.5
        command: redis-server /usr/local/etc/redis/redis.conf
        ports:
            - 6379:6379
        volumes:
            - ./redis.conf:/usr/local/etc/redis/redis.conf
    ```

- Up and Run

    ```bash
    $ docker-compose up -d
    ```

- Run command in a running container

    ```bash
    $ docker container exec -it redis /bin/sh
    ```

- Run redis-cli

    ```bash
    $ redis-cli -h [localhost](http://localhost) 
    ```

- Down and Stop

    ```bash
    $ docker-compose down
    ```

- Configuration file reference

    https://raw.githubusercontent.com/antirez/redis/6.0.5/redis.conf