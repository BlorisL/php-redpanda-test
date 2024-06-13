# To build and run containers

```sh
cd docker
docker-compose up -d --force-recreate --build
```

# To send a message from the browser

```url
http://localhost:8085/producer.php
```

# To receive a message

```sh
cd docker
docker exec -it docker-php-1 php -f ../consumer.php
```

[Share with me a cup of tea](https://www.buymeacoffee.com/bloris) ☕
