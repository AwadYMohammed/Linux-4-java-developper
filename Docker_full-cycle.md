After create the 
Dockerfile:
```xml
FROM openjdk:8-jdk-alpine
EXPOSE 8080
MAINTAINER Ahmed AlSalih
RUN mkdir -p /usr/java/app
WORKDIR /usr/java/app
COPY target/springboot-docker.war /usr/java/app
ENTRYPOINT ["java","-jar","springboot-docker.war"]
```
-------------------------------------------------
```xml
docker build -t <new-image-name> .
```
------------------------------------------------
```java
docker run -p 91:80 -- name web <imagename>
docker container run --name web -p 66:8080  -it -d spring-boot-docker
```
### list running Images
```cmd
docker images
```
### list all the running status
```xml
docker ps -a
```
-----------------------------------------------------------------------------------------
docker ps
rmi will not work because its running
# Remove the running container
```java
$ docker stop <NAMES>
$ docker rm <NAMES>
```
### Remove image
```
$ docker rmi <IMAGE ID>
```
OR

## Delete all running and stopped containers
```
$ docker container rm -f $(docker ps -aq)
$ docker rmi <IMAGE ID>
```
----------------------------------------------------------------------------------------
Go inside container
```
$ docker exec -it <container-id> /bin/sh
$ winpty docker exec -it <container-id> //bin//sh
```
----------------------------------------------------------------------------------------
## Print the last 100 lines of a container’s logs 
```
$ docker container logs --tail 100 web
```
```
docker run -d -it --name os ubuntu
```
-i mean this std is open <Standered Input is Open>
-t interactive processor 
-d detached mode / so the process will not be attached to the terminal if closed will killed

```
docker exec -it os bash
```
os = name of the docker 
bash = command lind inside the docker
```
mkdir test
exit
```
back to desktop
```
docker stop os
docker rm os
```
All the change in the docker container gone

without Dokerfile you can pull
docker pull ubuntu

nisepidine and latitain cream 4:29PM  4-29


power bi vs alteryx
how does alteryx process data
ventures
cdw data warehouse
fiona DATA LAKE