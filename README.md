# :whale: Docker for Local Dev Environment Setup

## Dev Environment List

:elephant: [Postgres](https://github.com/ariphidayat/docker-dev-environment/tree/master/postgres)


## Useful Commands

- Image List

    ```bash
    $ docker image ls -a
    ```

- Container List

    ```bash
    $ docker container ls -a
    ```

- Container Logs

    ```bash
    $ docker container logs [container name]
    ```

- Volume List

    ```bash
    $ docker volume ls
    ```

- Run Command in a running container

    ```bash
    $ docker container exec -it [container name] /bin/sh
    ```