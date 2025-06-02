# Feedback App with Flask Backend & Node.js Frontend on Kubernetes (Minikube)

This project is a simple feedback application featuring:

- **Flask backend** API to receive and serve feedback
- **Node.js frontend** for submitting feedback
- Deployment on **local Kubernetes cluster using Minikube**
- Dockerized services for backend and frontend

---

## Folder Structure

.
├── backend/ # Flask backend code & Dockerfile
│ ├── app.py
│ ├── Dockerfile
│ └── requirements.txt
├── frontend/ # Node.js frontend code & Dockerfile
│ ├── index.js
│ ├── package.json
│ └── Dockerfile
├── k8s/ # Kubernetes deployment & service YAMLs
│ ├── backend-deployment.yaml
│ ├── backend-service.yaml
│ ├── frontend-deployment.yaml
│ └── frontend-service.yaml
├── .gitignore
├── .dockerignore
├── README.md
└── ...



---

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- Node.js and npm (for frontend development)

---

## Setup and Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/AzamCloudOps/minikube-feedback-app

cd minikube-feedback-app

2. Start Minikube and configure Docker environment

minikube start
eval $(minikube docker-env)

3. Build Docker images inside Minikube

Build backend image:

cd backend
docker build -t feedback-backend:latest .
cd ..


Build frontend image:

cd frontend
docker build -t feedback-frontend:latest .
cd ..


4. Update Kubernetes deployment YAML files
Make sure k8s/backend-deployment.yaml uses:

image: feedback-backend:latest
and k8s/frontend-deployment.yaml uses:

image: feedback-frontend:latest

5. Deploy backend and frontend to Minikube

kubectl apply -f k8s/backend-deployment.yaml
kubectl apply -f k8s/backend-service.yaml

kubectl apply -f k8s/frontend-deployment.yaml
kubectl apply -f k8s/frontend-service.yaml

6. Check pods status
    kubectl get pods

7. Access frontend service
    minikube service feedback-frontend-service --url


---

Created By Mohd Azam Uddin

If you want, I can help you generate or update your k8s YAML files or frontend/backend code next!
