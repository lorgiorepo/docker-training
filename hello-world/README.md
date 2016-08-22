Run the container:
1. Run build.sh
2. List images with $docker images
3. Run up.sh
4. Open browser in http://[ip address listen by docker]:8090/
5. Close app and run $docker ps, it shows the image created

Manage container status:
1. Pause the docker container: $docker pause basic
2. Unpause the docker container: $docker unpause e50a4dfab2cb
3. Stop the docker container: $docker stop basic
4. Start the container: $docker start e50a4dfab2cb
5. Remove the container: $docker rm e50a4dfab2cb

Creating two container from the same image
1. docker run --name basic01 -p 8091:8080 nodebasic
2. docker run --name basic02 -p 8092:8080 nodebasic

Check the status of container:
1. docker ps

Kill and remove the containers
1. docker kill basic01 basic02
2. docker rm basic01 basic02

Checking the log:
1. docker logs basic

Login inside the container:
1. docker exec -it basic bash
2. exit
