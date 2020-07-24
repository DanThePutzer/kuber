[![DanThePutzer](https://circleci.com/gh/DanThePutzer/kuber.svg?style=svg)](https://github.com/DanThePutzer/kuber/tree/master)

# kuber

The repository showcases how to operationalize a machine learning microservice API with **Docker** and deploy it at scale using **Kubernetes**. The application consists of a pre-trained machine learning model built on `sklearn` and geared towards predicting house prices in the city of Boston. The focus of this project is on said operationalization and deployment. Therefore, the actual application being deployed has been provided by a third party.

![Container](https://user-images.githubusercontent.com/25454503/88419845-2418d200-cde6-11ea-9413-64cde8b95a50.png)

### Before You Start

Before everything can be run on your local machine a few things need to be in place. Please make sure that **Docker** is installed and running locally. Download it for your system [here](https://www.docker.com/products/docker-desktop). Additionally you need to have **minikube** as well as **kubectl** configured in order to set up and run a local Kubernetes cluster. Learn more about [minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/) and [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

&nbsp;

### Setup

A simple **Makefile** has been created to get you up and running quickly. Find a comprehensive list of the commands available through said **Makefile** below.

| **Command**                | **Description**                          |
|----------------------------|------------------------------------------|
| make **setup**             | Create proper python venv                |
| make **install**           | Install all necessary dependencies       |
| make **validate-circleci** | Validate CircleCI configuration file     |
| make **run-circleci**      | Run CircleCI locally to verify build     |
| make **lint**              | Lint Docker container and Python scripts |

&nbsp;

### Helper Scripts

A variety of bash scripts are provided to streamline certain tasks related to **Docker** containers and **Kubernetes** clusters.

| **Bash Script**        | **Description**                                                                            |
|------------------------|--------------------------------------------------------------------------------------------|
| **run_docker.sh**      | Builds and runs Docker container with port 80 exposed and forwarded to host port 8000      |
| **upload_docker.sh**   | Authenticates with Docker Hub and uploads finished Docker container                        |
| **run_kubernetes.sh**  | Runs Docker container on local Kubernetes cluster with port 80 forwarded to host port 8000 |
| **make_prediction.sh** | Runs test prediction to validate if everything is up and running correctly                 |


&nbsp;

### Important Files

There are few other important files to consider when working with this repo. The table below gives a short overview.

| **File**             | **Description**                                                                              |
|----------------------|----------------------------------------------------------------------------------------------|
| **app.py**           | Contains the actual machine learning model to be operationalized                             |
| **requirements.txt** | List of dependencies that need to be installed in container for the app to function properly |
| **Dockerfile**       | Configures how the Docker container should be built                                          |

&nbsp;

![Daniel Putzer, 2020](https://i.ibb.co/LSxTsY3/dan.png "Daniel Putzer, 2020")  
<https://danielputzer.com>
