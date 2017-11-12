# Docker Wordpress + Nginx + Mysql #

## Install ## 

### Docker ###
`sudo yum install docker` 

### Docker-compose ###
sudo curl -L https://github.com/docker/compose/releases/download/1.16.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose

`sudo chmod +x /usr/local/bin/docker-compose`

## Running ##
`sudo service docker start`

`sudo docker-compose up -d`

## Remove useless docker container ##
`sudo docker ps -a`

`sudo docker rmi $(docker images -q -f dangling=true)`

`sudo docker rm  $(docker ps -a -f status=exited  -q)`

`sudo docker volume rm $(docker volume ls -f dangling=true -q)`
