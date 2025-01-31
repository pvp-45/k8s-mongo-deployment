# Kubernetes Project: Deploy Web App with MongoDB

## Overview
This project marks my first experience with Kubernetes. Using **Minikube**, **kubectl**, and YAML, I deployed a web application connected to a MongoDB database. The project demonstrates the use of **ConfigMaps**, **Secrets**, **Deployments**, and **Services** for a functional Kubernetes setup.

---

## Project Components
1. **ConfigMap**: Stores the MongoDB service endpoint.  
   File: [`mongo-config.yaml`](mongo-config.yaml)

2. **Secret**: Stores sensitive credentials for MongoDB.  
   File: [`mongo-secret.yaml`](mongo-secret.yaml)

3. **MongoDB Deployment and Service**: Deploys MongoDB with an internal service.  
   File: [`mongo.yaml`](mongo.yaml)

4. **Web App Deployment and Service**: Deploys the web application with external access via NodePort.  
   File: [`webapp.yaml`](webapp.yaml)

---

## Tools Used
- **Kubernetes** for container orchestration.
- **Minikube** to create a local Kubernetes cluster.
- **kubectl** to manage Kubernetes resources.
- **YAML** for defining manifests.

---

## How to Use
1. Start Minikube:
   ```bash
   minikube start --driver=docker

2. Apply the manifests:
    ```bash
    kubectl apply -f mongo-secret.yaml
    kubectl apply -f mongo-config.yaml
    kubectl apply -f mongo.yaml
    kubectl apply -f webapp.yaml

3. Access the web app:

    ```bash
    http://<minikube-ip>:30100
Replace <minikube-ip> with the output of "minikube ip"

---   

## Key Learnings
1. Kubernetes components: Deployments, Services, ConfigMaps, Secrets.
2. Local cluster setup with Minikube.
3. Connecting applications in Kubernetes using Services.

This project is my first step into Kubernetes. Suggestions and feedback are welcome!