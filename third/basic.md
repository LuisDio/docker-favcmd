Environment variable in docker

export APP_COLOR=blue;
This way you can run multiple container of the same app with different parameter

docker run -e APP_COLOR=blue simple-webapp - run a container app with Environment variable

You can inspect Environment variable in the container to see if any implementation
