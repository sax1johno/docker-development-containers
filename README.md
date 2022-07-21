# Docker Development Containers
A listing of development environments packaged as docker containers, along with simple instructions for using them.

During development, you'll mount a local directory on your development machine as a volume in your development container.  This gives you a persistent artifact of the development process, while still allowing you to utilize the tools bundled with the container.

The example below will create a NodeJS development container, mount the current working directory `${PWD}` into the container as the `/usr/src` directory, and bind port 3000 on the container with port 3000 on the development machine.

Ex: docker run --rm -it -v ${PWD}:/usr/src -p 3000:3000 node:latest 

You can generally use the same pattern for all of these development machines, replacing the container tag (node:latest) with the containers below.

## W

* WasmEdge: `docker run -p 3000:3000 --rm -it -v ${PWD}:/usr/src wasmedge/appdev_x86_64:0.8.2`
