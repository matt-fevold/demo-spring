# What is this

Just a silly demo to get Spring up and running on a new linux laptop I setup.

I could simplify this quite a bit.

# How to run

build using this

`./gradlew build distTar`

build the docker container

`docker build --build-arg JAR_FILE=build/libs/*.jar -t demo-1 .`

run the container

`docker run demo-1`

find docker container id

`docker ps`

find the ip address 

`docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' [container id]`
