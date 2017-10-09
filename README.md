## Build ##

```
docker build -t warfox/jenkins-blueocean .
```

## Run ##

```
docker run -p 8080:8080 -p 50000:50000 -v /var/run/docker.sock:/var/run/docker.sock warfox/jenkins-blueocean
```

## Additional ##
You may have to run

```
docker exec -it --user=root container_name /bin/sh -c "chgrp jenkins /var/run/docker.sock"
```
