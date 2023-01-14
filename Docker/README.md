# Docker

### What is a container?
Simply put, a container is a sandboxed process on your machine that is isolated from all other processes on the host machine.
- is a runnable instance of an image. You can create, start, stop, move, or delete a container using the DockerAPI or CLI.
- can be run on local machines, virtual machines or deployed to the cloud.
- is portable (can be run on any OS).
- is isolated from other containers and runs its own software, binaries, and configurations.

### What is a container image?
- Container image contains the container’s filesystem, it must contain everything needed to run an application - all dependencies, configurations, scripts, binaries, etc.
- The image also contains other configuration for the container, such as environment variables, a default command to run, and other metadata.
