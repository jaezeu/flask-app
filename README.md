## Introduction

Note that this repository is only used for running a sample flask app

## Environment setup for running locally

Ensure that you have the following installed on your system:

- python 3.x
- pip

Create a virtual environment as this prevents package conflicts and keeps your setup clean:

```bash
cd flask_app
python3 -m venv venv
source venv/bin/activate

#Once the virtual environment is active, proceed with the following:
pip install --upgrade pip
pip install flask
```

You can then run your app within your virtual environment:

```bash
python app.py
```

## Building and running docker app

Ensure that you have the following 3 files in the directory where you are about to run the commands:

1) app.py
2) Dockerfile (https://docs.docker.com/engine/reference/builder/)
3) requirements.txt (https://pip.pypa.io/en/stable/reference/requirements-file-format/)

You may have to run the commands below in sudo if your user is not in a docker user group. To run docker as a non root user: https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user

```
# Build a docker image locally 
docker build -t flask-app .

# Listing your built images 
docker images

# Starting your local container with port mapping from host port to container port(-p) and in detached mode(-d)
docker run -d -p 8080:8080 flask-app

# List your running containers
docker ps

# List all your containers(Running and stopped)
docker ps -a

# To stop and remove your container
docker stop <container ID>
docker rm <container ID>

# To remove your docker images
docker rmi <image ID>

# To check your container logs
docker logs <container ID>

# To exec into your container
docker exec -it <container ID> /bin/bash

```

For all docker commands: https://docs.docker.com/engine/reference/commandline/cli/
