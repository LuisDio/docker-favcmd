Create docker image

```
FROM ubuntu ---> start from a base OS or another images

RUN apt-get update ---> install dependencies
RUN apt-get install python ---> install dependencies

RUN pip install flask ---> install dependencies
RUN pip install flask-mysql ---> install dependencies

COPY . /opt/source-code ---> copy source code from current dir

ENTRYPOINT FLASK_APP=/opt/source-code/app.py flask run ---> specify entry point

```


```docker build Dockerfile -t user/my-custom-webapp - Build the docker image```

```docker push user/my-custom-webapp```
