# :leaves: MongoDB

- Up and Run

    ```bash
    $ docker-compose up -d
    ```

- Container shell access

    ```bash
    $ docker exec -it mongo bash
    ```

- mongo shell client

    ```bash
    $ mongo --host localhost --port 27017
    ```

- Down and Stop

    ```bash
    $ docker-compose down
    ```

## MongoDB Cheat Sheet

- Show Databases

    ```bash
    > show databases
    ```

- Create and Use Database

    ```bash
    > use [database name]
    ```

- Database Methods

    [https://docs.mongodb.com/manual/reference/method/js-database](https://docs.mongodb.com/manual/reference/method/js-database/)

- MongoDB Collection
    - document storage
    - max document size is 16MB
    - max document nested level is 100
    - Create Collection

        ```bash
        > db.createCollection("collection_test")
        ```

    - Show Collections

        ```bash
        > db.getCollectionNames()
        ```

    - Get Collection

        ```bash
        > db.getCollection("collection_test")
        ```

    More info : [https://docs.mongodb.com/manual/reference/method/js-](https://docs.mongodb.com/manual/reference/method/js-database/)collection