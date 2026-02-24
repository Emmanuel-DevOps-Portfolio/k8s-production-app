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

## Architecture

This project follows a standard 3-tier architecture:

`User → NGINX → Backend → Database`

- NGINX exposed via Kubernetes Service
- Backend deployed as scalable Pods
- Database backed by PersistentVolumeClaims
- Internal communication via ClusterIP services and DNS

## Architecture Diagram 
`docs/architecture.png`
![Architecture](docs/architecture.png)

## Setup Instructions
1. Clone the repo:
```bash
git clone https://github.com/Emmanuel-DevOps-Portfolio/k8s-production-app.git
cd k8s-production-app
```
2. Apply manifests
```bash
kubectl apply -f manifests/
```
# Or Using Helm 
```bash
helm install myapp charts/myapp
```
3. Verify pods and services:
```bash
kubectl get pods -n <namespace>
kubectl get svc -n <namespace>
kubectl get hpa -n <namespace>
```

## Production Features Implemented
- Namespace-based workload isolation
- RBAC enforcement using least-privilege principles
- NetworkPolicies for pod-level traffic restriction
- Horizontal Pod Autoscaler (HPA) for dynamic scaling
- Liveness and readiness probes for health management
- Service-to-Pod communication using label selectors
- Internal cluster DNS validation
- Observability with Prometheus and Grafana

## Operational Debugging Experience
- Diagnosed and resolved `CrashLoopBackOff` conditions
- Troubleshot failed probe configurations
- Validated service endpoints and selector alignment
- Inspected pod events and controller reconciliation behavior

## Screenshots / Proof

Screenshots are available in the `/docs` directory:

- Grafana dashboards
- `kubectl get pods` output validation
- Helm release status verification


