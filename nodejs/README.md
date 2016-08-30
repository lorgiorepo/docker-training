### Create image container and verify
```sh
$ docker build -t nodelor .
$ docker images
```

### Link to exist docker redis container
```sh
$ docker run -d --name nodejs -p 8080 --link redis:redis nodejs
$ docker ps -a
```
