docker run -p 80:5000 container_name/simple-webapp - Port mapping allow to access the internal docker app running at 5000 to be accessible outside at port 80 of the host system

docker run -v /opt/datadir:/var/lib/mysql mysql - volume mapping allow to persist data contained inside the container to be outside the container
