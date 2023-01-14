# Docker

### Docker overview
Docker is an open platform for developing, shipping, and running applications.

### Docker architecture
- Docker uses a client-server architecture.
- The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers.
- The Docker client and daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon.
- The Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface.

![image](https://user-images.githubusercontent.com/102741020/212479005-f7796de3-b3ef-4854-a5ce-29e4efc18a00.png)

#### 1. The Docker daemon
The Docker daemon (dockerd) listens for Docker API requests and manages Docker objects such as images, containers, networks, and volumes. A daemon can also communicate with other daemons to manage Docker services.

#### 2. The Docker client
The Docker client (docker) is the primary way that many Docker users interact with Docker. When you use commands such as docker run, the client sends these commands to dockerd, which carries them out. The docker command uses the Docker API. The Docker client can communicate with more than one daemon.

#### 3. Docker registries
A Docker registry stores Docker images. Ex: Docker Hub or your own private registry

#### 4. Docker objects
When you use Docker, you are creating and using images, containers, networks, volumes, plugins, and other objects.

**Images** : An image is a read-only template with instructions for creating a Docker container. Often, an image is based on another image, with some additional customization.

## What is a container?
Simply put, a container is a sandboxed process on your machine that is isolated from all other processes on the host machine.
- is a runnable instance of an image. You can create, start, stop, move, or delete a container using the DockerAPI or CLI.
- can be run on local machines, virtual machines or deployed to the cloud.
- is portable (can be run on any OS).
- is isolated from other containers and runs its own software, binaries, and configurations.

### What is a container image?
- Container image contains the container’s filesystem, it must contain everything needed to run an application - all dependencies, configurations, scripts, binaries, etc.
- The image also contains other configuration for the container, such as environment variables, a default command to run, and other metadata.

## The underlying technology
Docker is written in the Go programming language and takes advantage of several features of the Linux kernel to deliver its functionality. Docker uses a technology called namespaces to provide the isolated workspace called the container. When you run a container, Docker creates a set of namespaces for that container.

These namespaces provide a layer of isolation. Each aspect of a container runs in a separate namespace and its access is limited to that namespace.
