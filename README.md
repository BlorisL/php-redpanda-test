# To build and run containers

cd docker
docker-compose up -d --force-recreate --build

# To send a message from the browser

http://localhost:8085/producer.php

# To receive a message

cd docker
docker exec -it docker-php-1 php -f ../consumer.php
