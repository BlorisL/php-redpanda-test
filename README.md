# Per buildare e far partire i container

cd docker
docker-compose up -d --force-recreate --build

# Per inviare un messaggio dal browser

http://localhost:8085/producer.php

# Per ricevere i messaggi

cd docker
docker exec -it docker-php-1 php -f ../app/consumer.php