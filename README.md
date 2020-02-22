[![CircleCI](https://circleci.com/gh/deepakmadisetty/microservices.svg?style=svg)](https://circleci.com/gh/noahgift/container-revolution-devops-microservices)

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

### Summary of Files
* app.py - Python file where the application code resides
* Dockerfile - Contains a set of commands used to build an image
* README.md - Contains extensive description about the project
* Makefile - Contains the set of directives used by build automation tools. It has 4 commands
    * setup - Creates and sources the virtual environment
    * install - I0nstalls the required libraries
    * lint - Lints the docker and pytyhon code
    * all - Runs all the above tasks
* requirement.txt - Prodvides the list of libraries required by the application
* run_docker.sh - This script will build, tag and run a docker image
* run_kubernetes.sh - Runs the docker image with kubernetes, also does port forwarding
* upload_docker.sh - Tags and uploads the docker image to the docker repository
* make_predictions.sh - Sends a request to the prediction app to provide a prediction 
* config.yml - CircleCI config file which builds , test the project automatically when changes are pushed
* docker_out.txt - Output of the prediction after executing run_docker.sh
* kubernetes_out.txt - Output of the prediction after executing run_kubernetes.sh 
