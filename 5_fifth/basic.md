Docker CMD vs ENTRYPOINT

```
CMD command param - default command to run

ENTRYPOINT - specify the program that will be run when the container start

FROM ubuntu

ENTRYPOINT["sleep"]

CMD["5"]

```
finale command run is sleep 5
