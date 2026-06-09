# Kubernetes NGINX Project

## Overview

This project demonstrates a complete Kubernetes NGINX deployment with important Kubernetes resources connected together for practical DevOps learning.

The project includes:

* Pod
* Deployment
* Service
* Ingress
* ConfigMap
* Secret
* Persistent Storage
* StatefulSet
* DaemonSet
* CronJob
* Horizontal Pod Autoscaler
* RBAC Configuration

---

# Technologies Used

* Kubernetes
* Docker
* NGINX
* YAML
* kubectl

---

# Project Architecture

The application is deployed inside the `nginx-app` namespace.

The Deployment manages NGINX Pods and exposes them using a Kubernetes Service. Ingress handles external routing to the application. ConfigMaps and Secrets manage environment variables and sensitive data. PersistentVolumeClaim provides storage for containers.

Additional Kubernetes resources like StatefulSet, DaemonSet, CronJob, HPA, and RBAC are included for learning advanced Kubernetes concepts.

---

# Files Description

| File Name        | Description                               |
| ---------------- | ----------------------------------------- |
| namespace.yaml   | Creates Kubernetes namespace              |
| pod.yaml         | Creates standalone NGINX Pod              |
| deployment.yaml  | Manages NGINX application replicas        |
| service.yaml     | Exposes application internally/externally |
| ingress.yaml     | Routes external traffic                   |
| configmap.yaml   | Stores environment configuration          |
| secret.yaml      | Stores sensitive credentials              |
| pvc.yaml         | Persistent storage request                |
| statefulset.yaml | Stateful application deployment           |
| daemonset.yaml   | Runs pod on all worker nodes              |
| cronjob.yaml     | Scheduled Kubernetes jobs                 |
| hpa.yaml         | Automatic pod scaling                     |
| rbac.yaml        | Access control configuration              |

---

# Deployment Steps

## Create Namespace

```bash
kubectl apply -f namespace.yaml
```

## Deploy Configurations

```bash
kubectl apply -f configmap.yaml
kubectl apply -f secret.yaml
kubectl apply -f pvc.yaml
```

## Deploy Application

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f ingress.yaml
```

## Deploy Additional Resources

```bash
kubectl apply -f statefulset.yaml
kubectl apply -f daemonset.yaml
kubectl apply -f cronjob.yaml
kubectl apply -f hpa.yaml
kubectl apply -f rbac.yaml
```

---

# Useful Commands

## Check Pods

```bash
kubectl get pods -n nginx-app
```

## Check Services

```bash
kubectl get svc -n nginx-app
```

## Check Deployments

```bash
kubectl get deployments -n nginx-app
```

## View Logs

```bash
kubectl logs <pod-name> -n nginx-app
```

---

# Learning Objectives

This project helps in understanding:

* Kubernetes Architecture
* YAML Configuration
* Pod Management
* Networking
* Storage
* Scaling
* Security
* Monitoring Basics
* Production Deployment Concepts

---

# Author

Abhijeet Patel

DevOps & Cloud Enthusiast
