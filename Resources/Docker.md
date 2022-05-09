# Docker commands
## Docker install
* [MAC](https://docs.docker.com/desktop/mac/install/)
* [Windows](https://docs.docker.com/desktop/windows/install/)
* [Linux](https://docs.docker.com/engine/install/ubuntu/)
* [Docker Compose](https://docs.docker.com/compose/install/)


## Basics
```
# Vericied cli can talk to engine
docker version

# Most Config Values of engine
docker info

# Help docker container
docker container --help

```

## Docker_system_commands
```
# Clean up just "dangling" images
docker image prune

# Clean up just "dangling" images
docker system prune

# Remove all images you're not using!!
docker system prune -a

# See space usage
docker system df

```

## Dockerfile template
[dockerfile - get started](https://docs.docker.com/get-started/)
[Environment replacement - dockerfile references](https://docs.docker.com/engine/reference/builder/#environment-replacement)
```
FROM busybox
ENV FOO=/bar
WORKDIR ${FOO}   # WORKDIR /bar
ADD . $FOO       # ADD . /bar
COPY \$FOO /quux # COPY $FOO /quux

```

## docker-compose template
[Overview of Docker Compose](https://docs.docker.com/compose/)
```
version: "3.9"  # optional since v1.27.0
services:
  web:
    build: .
    ports:
      - "5000:5000"
    volumes:
      - .:/code
      - logvolume01:/var/log
    links:
      - redis
  redis:
    image: redis
volumes:
  logvolume01: {}

```

## Docker_container_commands
```
# Run docker container and publish local port 80 to docker's port
--publish
docker container run -p 80:80 nginx

# Detach means run in background
--detach
docker container run -d -p 80:80 nginx

# Name of container
--name
docker container run -d -n my_nginx_name -p 80:80 nginx

# list of all running containers
docker container ls

# list of all running containers
docker container ls -a

# docker stop <first_3_digit_id> - stop running container
docker container stop 27d

# Watch logs of the container
docker container logs <name_of_container>

# top -- Display the running processes of a container
docker container top <name_of_container>

# Remove one or more containers. -f = force#
docker container rm <first_3_digit_id> -f

# Inspect -- Display detailed information on one or more containers
docker container inspect <name_of_container>

# stats -- Display a live stream of container(s) resource usag
docker container stats

# Start new container interactively
docker container run -it <shell>

# execute interactively in an existing container
docker container exec -it <shell>

# Start existing image and interactively attach to it
docker container start -ai <name_of_container>

# Named Volume
# ... run -v <name_of_volume>:<path/in/container> mysql
docker container run -d --name mysql -e MYSQL_ALLOW_EMPTY_PASSWORD=True -v mysql-db:/var/lib/mysql mysql

# Bind Mounting creation #
docker container run -d --name nginx -p 80:80 -v ${pwd}:/usr/share/nginx/html nginx

```


## Docker_Image_commands
```
# Show the history of an image
docker image history <name_of_image>

# Display detailed information on one or more images
docker image Inspect <name_of_image>

# Create a tag TARGET_IMAGE that refers to SOURCE_IMAG
docker image tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]
docker image tag nginx maorw/nginx

```

## Docker_Networks_commands
```
# Check ports of a container
docker container port <name_of_container>

# Get IP Address of conatainer, using a special format of inspect
## In Windows, you'll need to use double quote rather then a single quotes for --format 
docker container inspect --format "{{ .NetworksSetting.IPAddress }}" <name_of_container>

# List networks
docker network ls

# Inspect a network
docker network inspect

# Create a nwtwork
docker network create 

# Attach a network to container
docker network connect <network_name> <name_of_container>

# Detach a network from container
docker network disconnect

# Run new container with a particular network
docker container run -d --name new_nginx --network my_app_net nginx

# Give container an network alias for round robin
docker run -d --network my_test_net  --network-alias search elasticsearch:2

```

## Docker_volume_commands
```
# List volumes
docker Volume ls

# Create a Volume
docker volume create 

# Run  a container with a volume
... run -v mysql-db:/var/lib/mysql

```

## Docker Bind Mouning Commands
```
# Set Bind Mounting when creating a Container
... run -v //c/Users/hostUser/path:/path/conatiner
... run -v ${pwd}:/usr/share/nginx/html 

With Docker CLI, you can always use a full file path on any OS, 
but often you'll see me and others use a "parameter expansion" 
like $(pwd) which means "print working directory".

Here's the important part. Each shell may do this differently, so here's a cheat sheet for which OS and Shell your using. I'll be using $(pwd) on a Mac, but yours may be different!

This isn't a Docker thing, it's a Shell thing.

For PowerShell use: ${pwd} 

For cmd.exe "Command Prompt use: %cd%

Linux/macOS bash, sh, zsh, and Windows Docker Toolbox Quickstart Terminal use: $(pwd) 

```

## Dockerfile commands
```

# Execute from a Dockerfile which are at the same directory
docker image build -t customimage .

# -f flag -- Name of the Dockerfile (Default is 'PATH/Dockerfile')
docker image build -f some-dockerfile

```
## Docker-compose Commands

```
# Setup Volumes/networks and start all containers 
docker-compose up # -d for detach


Rebuild single container

docker-compose up -d --no-deps --build <service_name>
Enter the container

docker-compose exec [service name] bash

# List running compose projects 
docker-compose ls

# List Containers 
docker-compose ps

# Display the running processes 
docker-compose top

# Stop all containers and remove cont/vol/net 
docker-compose down

```

## DockerHub access
```
# Login
docker Login

# Modify the login config
cat .docker/config.json


# Push docker image with tag to your hub
docker image push maorweissb/nginx

# Logout
docker logout
```