#Hello world express app inside container

This is a basic docker container with an express app. There is some docker commands to manage the state.

### Create container
```sh
$ docker build -t nodebasic .
$ docker images
```

### Run the container

```sh
$ docker run --name basic -p 8090:8080 nodebasic
$ docker ps
```

Open browser in http://[ip address listen by docker]:8090/ and then close app

### Manage container status

Pause the docker container with name:
```sh
$ docker pause basic
```

Unpause the docker container with Id:
```sh
$ docker unpause e50a4dfab2cb
```

Stop the docker container with name:
```sh
$ docker stop basic
```

Start the container with Id:
```sh
$ docker start e50a4dfab2cb
```

Remove the container with Id:
```sh
$ docker rm e50a4dfab2cb
```

### Containers from the same image

Creating two container with the same image:

```sh
$ docker run --name basic01 -p 8091:8080 nodebasic
$ docker run --name basic02 -p 8092:8080 nodebasic
```

Kill and remove the containers:

```sh
$ docker kill basic01 basic02
$ docker rm basic01 basic02
```

Checking the log:

```sh
$ docker logs basic
```

### Inside Containers

Login inside the container:

```sh
$ docker exec -it basic bash
$ exit
```

```sh
$ docker run -it ubuntu bash
$ exit
```
