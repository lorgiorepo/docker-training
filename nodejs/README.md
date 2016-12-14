### Create image container and verify
```sh
$ docker build -t nodejs .
$ docker images
```

### Link to exist docker redis container
```sh
$ docker run -d -p 80:8080 --name nodejsio --link redisio nodejs
$ docker ps -a
```
