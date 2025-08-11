# assignment-5
ocal Kubernetes Deployment with Minikube
This project demonstrates how to deploy, manage, and expose a simple NGINX web server on a local Kubernetes cluster using Minikube. This serves as a foundational exercise for understanding Kubernetes concepts like Deployments and Services.

## Overview
The objective is to create a multi-pod NGINX deployment and make it accessible from the local machine. This is achieved by defining the application's state declaratively using YAML configuration files and managing it with kubectl.

Key Tools Used:

Kubernetes
Minikube (for local cluster creation)
Docker (as the container runtime for Minikube)
kubectl (for interacting with the cluster)
## How to Run This Project
### Prerequisites
Docker installed and running.
Minikube installed.
kubectl installed.
### Steps
Clone the Repository

git clone [https://github.com/pavanyarrapragada03/devops-internship-task-5.git](https://github.com/pavanyarrapragada03/devops-internship-task-5.git)
cd devops-internship-task-5
Start the Minikube Cluster

minikube start
Deploy the NGINX Application Apply the deployment and service configurations to the cluster. The deployment will create the pods, and the service will expose them.

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
Access the Application Minikube provides a simple command to get the URL and open it in your browser.

minikube service my-nginx-service
This will open the NGINX welcome page.

## Verification Commands
Here are some useful commands to check the status of your deployment.

Check all resources (pods, services, deployments):

kubectl get all
Scale the deployment to 3 replicas:

kubectl scale deployment my-nginx-deployment --replicas=3
View detailed information about a specific pod:

# First, get the pod name with kubectl get pods
# Then, use the name in the command below
kubectl describe pod my-nginx-deployment-5564bc5c84-856dd
## Final Result
Here is a screenshot of the NGINX welcome page running successfully after being accessed through the Minikube service.

Add your screenshot here by creating a folder named screenshots, adding your image to it, and referencing it like this: ![NGINX Welcome Page]
