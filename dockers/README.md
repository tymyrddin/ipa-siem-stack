# Docker Image Builder

The creation of the images for the stack deployment in Docker is done with the `build-images.yml` script

To execute the process, the following must be executed in the root of the `docker` repository. You may have to run it twice, first with sudo to create the `.env` file, then without to build the images:

```
$ build-docker-images/build-images.sh
```

This script initializes the environment variables needed to build each of the images, then calls `docker compose` to build the images.
We may want to split this in the future.
