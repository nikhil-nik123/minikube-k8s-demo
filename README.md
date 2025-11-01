# Minikube Kubernetes Setup

This project contains configuration files to deploy and expose a simple Nginx service on Minikube using Kubernetes.

## Files
- **deployment.yaml** — Defines Nginx deployment.
- **service.yaml** — Exposes the deployment via a NodePort or ClusterIP.
- **main.tf** — Terraform configuration (if used for infra setup).

## Commands Used
```bash
minikube start
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl port-forward svc/my-nginx-service 55000:80
