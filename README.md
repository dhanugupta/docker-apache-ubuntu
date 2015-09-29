# Docker with Apache Ubuntu PHP
Installing Docker You can click here <a href="https://docs.docker.com/installation/#installation" target="_blank">Docker Installation</a>

Setting up the project
./Dockerfile
./app/index.php
./apache-config.conf

Building the container
docker build -t app .

Running the container
docker run -d -p 80:80 -v /data/server/app:/var/www/site/app --name app app

Logging into the container
docker exec -it app bash

Stop/Remove the container
docker stop app
docker rm app
