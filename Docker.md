### Docker

#### Concepts

1. **Image**: is an executable package that includes everything needed to run an application--the code, a
   runtime, libraries, environment variables, and configuration files.
2. **Container**: is a runtime instance of an image--what the image becomes in memory when executed (that is, an image with state, or a user process). You can see a list of your running containers with the command, `docker ps`, just as you would in Linux. A **container** runs *natively* on Linux and shares the kernel of the host machine with other containers. It runs a discrete process, taking no more memory
   than any other executable, making it lightweight.

#### Command sheet

1. `docker --version`: Display docker version;
2. `docker version`: Display information about  both docker client and server versions;
3. `docker info`: Display **extra** information about  both docker client and server;
4. `docker ps`: List running containers;
5. `docker container ls`: List containers (running, all, all in quiet mode);
   1. `docker container ls --all`: List **all** containers;
   2. `docker container ls -aq`: List containers all in quiet mode;
6. `placeholder`: ;