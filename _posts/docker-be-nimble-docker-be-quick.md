---
published: false
---

## Stopping Containers
Need to stop a docker container? There's a couple ways of doing it, but each have some subtleties:

Need to be graceful?
> docker stop {container}

Just die... now, please
> docker kill {contianer}

Go away - forever
> docker rm -f {container}