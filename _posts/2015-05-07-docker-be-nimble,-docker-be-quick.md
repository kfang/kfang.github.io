---
published: true
---

## Stopping Containers
Need to stop a docker container? There's a couple ways of doing it, but each have some subtleties:

Need to be graceful? send SIGTERM, and then SIGKILL after grace period
>docker stop {container}

Just die... now, please! send SIGKILL, or specified signal
>docker kill {contianer}

Go away - forever! send SIGKILL and then remove the container
>docker rm -f {container}