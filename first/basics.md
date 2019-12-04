docker run - start an instance container(add the image name)

docker ps - list container running container (add -a to list all with no exception)

docker stop - stop a container(add name or id to specify the container to be stopped)

docker rm - delete the container(add name or id to specify the container to be removed)

docker images - list all the image present in the host

docker rmi - remove the image(add the name of the image or its id)

docker pull - download the image without running it

docker exec - execute a command in the running container(add name or id to specify the container and the cmd to execute)

docker exec sally_cont cat /etc/host

docker run -d container_name - run a container in detach mode/or background mode(usually for container with log)

docker attach container_name - allow you to attach back to the container

docker run -it container_name bash - persist the container base image and log you into bash

docker run image:tags - run a container with a tags version( if not specified it will run latest)

docker run -it container_name - run container while listening to standard input and attached to terminal(-i interactive mode, -t terminal mode) if any.
