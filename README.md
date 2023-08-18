# Docker configuration for Symfony projects

*(Linux, NGINX, PHP^8, Symfony^6, Xdebug, PHPUnit)*

## How to use
1.Build Docker images based on the configuration defined in the docker-compose.yml
    
    make build (docker-compose build) 

2.Start containers and run composition for all services defined in the docker-compose.yml

     make up (docker-compose up)

3.Stop and delete containers
    
    make down (docker-compose down)

4.Enter to your container (bush)
    
    make app_bash  (docker-compose exec -u www-data php bash)

## How to connect to servers

| NGNIX SERVER           | Database | 
|------------------------|:--------:|
| https://localhost:8080 |    -     | 

##  Database config

| DATABASE | USER | PASSWORD |
|----------|:----:|---------:|
| -        |  -   |        - |

<hr>

## How to install Symfony in Docker container
*( [!] You must delete the <b>/app</b> folder [!] )*

1.Start the container

    make up (docker-compose up)

2.Enter to your container

    make app_bash  (docker-compose exec -u www-data php bash)

3.Create Symfony app

    symfony new app


## How to configure XDebug in PHPSTORM

1.Create an Xdebug server
![create xdebug server](https://raw.githubusercontent.com/gitEugeneL/Docker-Symfony/main/readme-img/create-server.png)

2.Config Xdebug server and Enjoy the work of Xdebug server
![Config xdebug server](https://raw.githubusercontent.com/gitEugeneL/Docker-Symfony/main/readme-img/config-server.png)


## Links

* [Docker](https://developer.fedoraproject.org/tools/docker/about.html) how to install Docker
* [Docker Compose](https://developer.fedoraproject.org/tools/docker/compose.html) how to install docker-compose
* [Symfony](https://symfony.com) Symfony
