# :postbox: Redis

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
    $ redis-cli -h localhost
    ```

- Down and Stop

    ```bash
    $ docker-compose down
    ```

- Configuration file reference

    https://raw.githubusercontent.com/antirez/redis/6.0.5/redis.conf


## Configuration Note

- Network Security

    go to **`NETWORK`**  section in **redis.conf** file, `bind` one or more IP addresses if you want listens from spesific IP addresses or comment all bind to listens for connections from all the network interfaces.

    `protected-mode yes` to avoid open accessed and exploited on the internet.

- Authentication and Authorization

    add ACL rule on  **`SECURITY`** section in **redis.conf** file with the following format:

    ```
    user [username] ... acl rules ... >[password]
    ```

    :bulb: Should add default user +@connection for auth process

- Client Connection

    ```bash
    # redis-cli -h [redis server host or docker container name]
    [redis-server]:6379> auth [username] [password]
    ```