# Docker with Apache Ubuntu PHP
Installing Docker You can click here <a href="https://docs.docker.com/installation/#installation" target="_blank">Docker Installation</a>

<h1>Setting up the project</h1>
<ul>
<li>./Dockerfile </li>
<li>./app/index.php</li>
<li>./apache-config.conf</li>
</ul>

<h1>Building the container</h1>
docker build -t app .

<h1>Running the container</h1>
docker run -d -p 80:80 -v /data/server/app:/var/www/site/app --name app app

<h1>Logging into the container</h1>
docker exec -it app bash

<h1>Stop/Remove the container</h1>
docker stop app
docker rm app

<h1>Volume logs of container to host</h1>
docker run -d -p 80:80 -v /data/server/app:/var/www/site/app -v /data/server/log:/var/log/apache2 --name app app 
