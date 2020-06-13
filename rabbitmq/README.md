# :rabbit: RabbitMQ

## Installation

- Compose file

    ```yaml
    version: '3.5'

    services:
      rabbitmq:
        container_name: rabbitmq
        image: rabbitmq:3.8.4-management
        environment:
            RABBITMQ_DEFAULT_USER: arip
            RABBITMQ_DEFAULT_PASS: rahasia
        ports: 
            - 5672:5672
            - 15672:15672
        volumes: 
            - data:/var/lib/rabbitmq

    volumes: 
        data:
    ```

- Up and Run

    ```bash
    $ docker-compose up -d
    ```

- Down and Stop

    ```bash
    $ docker-compose down
    ```