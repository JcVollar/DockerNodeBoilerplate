/// THE BASICS

# Build the image
$ docker build . -t myapp

# List all images
$ docker images

# Run the image
$ docker run -p 49160:8080 -d myapp

# Get container ID
$ docker ps

# Print app output
$ docker logs <container id>

# Example
Running on http://localhost:49160

# Enter the container
$ docker exec -it <container id> /bin/bash

# Kill our running container
$ docker stop <container id>

# Remove a container(you cannot remove running containers)
$ docker rm <container id>

# Removes every image that is not in use
$ docker image prune -a





/// More complex options
# Run the image
$ docker run -p 49160:8080 -d --rm --name mycontainername -v "C:/Users/jcvol/Desktop/Ny mappe":/usr/src/app -v /usr/src/app/node_modules  myapp 

