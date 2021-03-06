# Docker web development Node 8
This container can be used for doing all your node web development needs. Like running unit tests, linting, creating coverage reports and running your application.

## Software installed:
Node 8 and for more information about the installed tools se the [readme](../base/README.md) of the base image.

## Verify installation
The verify the node installation:
```bash
docker run -it --rm richardregeer/web-development:node-8 node -v
```

## How to use the container
Use a shared volume from a data container or host volume to share your code and start the program on the container.
Make sure the -rm option is used to destroy the container when it's finished.

Port 3000 is exposed and can be used for development.

```bash
# Start a node application in the container.
docker run -it --rm --volume=</path/to/your/code>:/development richardregeer/web-development:node-8 node <your-application.js>
```