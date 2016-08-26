# Set the base image to ubuntu
FROM        ubuntu

# File Author / Maintainer
MAINTAINER  Lorgio Trinidad

# Update the repository and install redis server
RUN         apt-get update && apt-get install -y redis-server

# Expose default Redis port 6379
EXPOSE      6379

# Run Redis server
ENTRYPOINT  ["/usr/bin/redis-server"]
