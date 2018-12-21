### Docker

#### Concepts

1. **Image**: is an executable package that includes everything needed to run an application--the code, a
   runtime, libraries, environment variables, and configuration files.
2. **Container**: is a runtime instance of an image--what the image becomes in memory when executed (that is, an image with state, or a user process). You can see a list of your running containers with the command, `docker ps`, just as you would in Linux. A **container** runs *natively* on Linux and shares the kernel of the host machine with other containers. It runs a discrete process, taking no more memory
   than any other executable, making it lightweight.

#### Command sheet

##### Application

1. `docker --version`: Display docker version;
2. `docker version`: Display information about  both docker client and server versions;
3. `docker info`: Display **extra** information about  both docker client and server;

##### Images

1. `docker images`: List all images;
2. `docker rmi <imageRepository | IMAGE ID>`: Remove specified image;

##### Containers

1. `docker ps`: List running containers;
   1. `docker ps -a`: List all containers;
2. `docker container ls`: List containers (running, all, all in quiet mode);
   1. `docker container ls --all`: List **all** containers;
   2. `docker container ls -aq`: List containers all in quiet mode;
3. `docker run -it [--detach] --name <containerName> --publish <[ip]:hostPort>:<[ip]:containerPort> <imageName> bash`: creates a container called `containerName` using `<imageName>` image  and binds `<hostPort>` into `<containerPort>`;
   1. `--detach`: makes docker detach from container immediately after its startup;
4. `[Ctrl] + { [p], [q] }`: detaches from current container;
5. `docker attach <containerName> `: attaches to  `<containerName> ` container;
6. `docker rm <containerName>`: remove the `containerName` container;
7. `docker build -t <imageName> .`: Read the `Dockerfile` in current directory and creates a image named `<imageName>`;
8. `docker exec -it <containerName> ...`: runs `...` commands on the running `<containerName>` container;
9. `docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <containerName>`: show the IP address of `<containerName>` container;

##### Networks

1. `docker network ls`: list networks;
2. `docker network create <networkName>`: creates a network called `<networkName>`;
3. `docker network rm  <networkName1>[ <networkName2> ... <networkNameN>]`: remove all network in given list;
4. `docker network prune`: remove all unused networks;

### References

1. [docs.docker.com - | Docker Documentation](https://docs.docker.com/engine/reference/run/#operator-exclusive-options)
2. [medium.com - Lifecycle of Docker Container – Nitin Agarwal – Medium](https://medium.com/@nagarwal/lifecycle-of-docker-container-d2da9f85959)
3. [stackoverflow.com - How to get a Docker container's IP address from the host? - Stack Overflow](https://stackoverflow.com/questions/17157721/how-to-get-a-docker-containers-ip-address-from-the-host)