# Docker Node

It's been a while since I've worked with docker. So I created a basic setup for a node application with express. 
It should be a basic git-pull, docker build and docker run to setup the basic development project. 
Remember to change the bind mount from my "C:/Users/jcvol/Desktop/Ny mappe" to wherever you run your code. Also give it some better names than mycontainername and myapp. 




# Run the image
> git pull

> docker build . -t myapp

> docker run -p 49160:8080 -d --rm --name mycontainername -v "C:/Users/jcvol/Desktop/Ny mappe":/usr/src/app -v /usr/src/app/node_modules  myapp 




# Basic Docker commands

Build the image
> docker build . -t myapp

List all images
> docker images

Run the image
> docker run -p 49160:8080 -d myapp

Get container ID
> docker ps

Print app output
> docker logs <container id>

Example
> Running on http://localhost:49160

Enter the container
> $ docker exec -it <container id> /bin/bash

Kill our running container
> docker stop <container id>

Remove a container(you cannot remove running containers)
> docker rm <container id>

Removes every image that is not in use
> docker image prune -a




