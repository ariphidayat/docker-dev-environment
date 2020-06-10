# :elephant: Postgres

- Up and Run

    ```bash
    $ docker-compose up -d
    ```

- Run Command in a running container

    ```bash
    $ docker container exec -it postgres /bin/sh
    ```

- Run psql

    ```bash
    # psql -U postgres
    ```

- Down and Stop

    ```bash
    $ docker-compose down
    ```