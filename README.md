NAME:Kariveda Neha Nandini
COMPANY:CODETECH IT SOLUTIONS
ID:CT08RYI
DOMAIN:Devops
DURATION:february 5th to march 5th 2025
MENTOR:neela santhosh

Kubernetes Deployment Overview

Introduction

A Kubernetes Deployment is a resource that manages and automates the deployment of containerized applications in a Kubernetes cluster. It ensures that the desired number of application instances (pods) are running, enables updates without downtime, and supports rollback in case of failure.

Key Features

Declarative Configuration: Define the desired state in a YAML file, and Kubernetes ensures it is met.

Scaling: Easily scale applications up or down by adjusting the number of replicas.

Rolling Updates: Update applications gradually without downtime.

Rollbacks: Revert to a previous version if an update fails.

Self-Healing: Automatically replaces failed or unhealthy pods.


Basic Deployment Example

apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-app
spec:
  replicas: 3
  selector:
    matchLabels:
      app: my-app
  template:
    metadata:
      labels:
        app: my-app
    spec:
      containers:
        - name: my-app-container
          image: my-app-image:latest
          ports:
            - containerPort: 80

Deployment Commands

Apply Deployment

kubectl apply -f deployment.yaml

Check Deployment Status

kubectl get deployments

Scale Deployment

kubectl scale deployment my-app --replicas=5

Update Deployment

kubectl set image deployment/my-app my-app-container=my-app-image:v2

Rollback Deployment

kubectl rollout undo deployment/my-app

Delete Deployment

kubectl delete deployment my-app

Conclusion

Kubernetes Deployments simplify the management of containerized applications by providing automated scaling, updates, and fault tolerance. They are essential for maintaining reliable and efficient applications in a Kubernetes environment.


---

This README provides a basic overview. For advanced configurations and best practices, refer to the official Kubernetes documentation.








