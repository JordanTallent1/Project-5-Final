## circleci (Badge) : [![CircleCI](https://circleci.com/gh/JordanTallent1/Project-5-Final.svg?style=svg)](https://circleci.com/gh/JordanTallent1/Project-5-Final)

## Python Commands
* To run the python script (app.py) I utilized the dockerfile:
* CMD [ "python", "app.py"]
* The other python related installations were installing tools using pip and creating the virtual environment 
* python3 -m venv ~/.devops
* source ~/.devops/bin/activate

## Defining Files
* Dockerfile - This is used to create an image from step by step calls defined by a user in this case (me).
* Makefile - This does a setup/install/test of requirements defined by the user.
* app.py -  The application to run in our environment that makes prediction percentage (up/down) on the housing market.
* make_prediction.sh - runs inputs through the app.py and returns a prediction percentage (up/down) of the housing prices in Boston.
* model_data - holds all data related to the app.py used for the machine learning program.
* requirements.txt - these are all the necessary environment packages/updates for your application to work properly.
* run_docker.sh - this is used to build/run the docker image, list the docker images, and expose the proper ports/terminal to the docker file that you are running. 
* run_kubernetes.sh - This creates a pod running your docker image and opens the proper port forwarding to your docker machine and list all the pods in the node. 
* upload_docker.sh - This uploads the latest docker build to your docker hub so that you can pull it and run it in your kubernetes pod.


## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
