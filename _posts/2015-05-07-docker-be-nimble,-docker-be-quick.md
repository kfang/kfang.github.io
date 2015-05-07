---
layout: post
published: true
---

## Running Containers
At the most basic level, you just need
> docker run {image}

But lets say, you want to name it?
> docker run --name {my-container-name} {image}

Or need to forward a port? The first number is the host port, the second is the container's port.
> docker run -p 8080:8080 {image}

Or maybe environment variables?
> docker run -e {ENV_VAR}={ENV_VALUE} {image}

## Stopping Containers
Need to stop a docker container? There's a couple ways of doing it, but each have some subtleties:

Need to be graceful? send SIGTERM, and then SIGKILL after grace period
> docker stop {container}

Just die... now, please! send SIGKILL, or specified signal
> docker kill {contianer}

Go away - forever! send SIGKILL and then remove the container
> docker rm -f {container}

## What's Running!?!?
> docker ps

## Lemme just step inside and take a look around...
> docker exec -it {container} /bin/bash