Information:

This is the Account Rest Service which exposed an endpoint "/myAccounts".
It is a post service through which a customer can get details of his/her account by providing the customer id.

Tech Stack:

Internally the program is using H2 database provided by springboot and you can refer the tables in the data.sql file.
The program is also using Docker concepts .

Docker:

1. To create a docker image , you need to provide image configuration in the pom.xml file and to generate the Docker file : "mvn spring-boot:build-image" needs to be run.
(Info:This command internally uses buildpacks(packeto) to generate docker image)


Some Useful commands of Docker:

1.docker images : This command list downs all the docker images created.
2.docker ps: This command list downs all the active docker containers.
(Info: doscker ps -a : List downs all the active and stopped containers)
3.docker stop {hashId of docker container}: This will stop the running of the docker mentioned
4.docker kill {hashId of docker container}: This will instantly kill the container.
5.docker logs {hashId of docker container}: To see all the logs of the application running in the container
(Info:To see continous logs of a container give docker logs -f (f means follow))
6.docker container pause {hashId of docker container}: This will pause the container 
7.docker container unpause {hashId of the docker container}: To unpause the container
8.docker container inspect {hashId of the docker container}: To inspect a container 
9.docker stats: it will give all the statistics of docker(Ex. Memory , CPU Utilization etc)
10.docker rm {hashId of the container}: To remove the container (Delete)
11.docker build {location of the docker file} -t {image name}
(Info : -t to give tag to an image)
12.docker push docker.io/{image name}: This command is used to push your image in docker hub

Docker compose
docker compose is used to start , stop etc. on many number of images together.
This can be achieved by creating a yaml file which contains all the necessary details.

1.docker-compose --version : To check if docker compose is present otherwise you have to install it.'
