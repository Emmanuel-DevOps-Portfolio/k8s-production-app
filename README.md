# Kubernetes Production App

## Project Goal
Deploy a production-style 3-tier application on Kubernetes with scaling, observability, and security features.

## Tech Stack
- Kubernetes
- Helm
- Docker
- Prometheus & Grafana
- Nginx (Frontend)
- PostgreSQL/MySQL (Database)

## Architecture Diagram
Include diagrams in `docs/architecture.png` and reference them here:
![Architecture](docs/architecture.png)

## Setup Instructions
1. Clone the repo:
```bash
git clone https://github.com/Emmanuel-DevOps-Portfolio/k8s-production-app.git
```
2. Apply manifests or Helm chart:
```bash
kubectl apply -f manifests/
# OR
helm install myapp charts/myapp
```
3. Verify pods and services:
```bash
kubectl get pods -n <namespace>
kubectl get svc -n <namespace>
```
What I Learned
- Configured namespaces, RBAC, and NetworkPolicies
- Implemented HPA for scaling
- Debugged CrashLoopBackOff & probe failures

Screenshots / Proof
Add images in docs/ and link here:
- Grafana dashboards
- kubectl get pods outputs
- Helm release status


