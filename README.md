# Kubernetes Deployments

A collection of Kubernetes deployment projects demonstrating the implementation of containerized applications using modern cloud-native technologies. This repository showcases end-to-end deployment workflows, networking, storage, configuration management, and production-ready Kubernetes concepts on both local and managed Kubernetes clusters.

---

## Repository Structure

| Project | Architecture | Platform | Description |
|----------|-------------|----------|-------------|
| **2-tier-app** | Frontend + Backend | AWS EC2, Kind, MetalLB | Two-tier application deployment with Kubernetes Services, NGINX reverse proxy, and internal service communication. |
| **3-tier-app** | Frontend + Backend + Database | Amazon EKS, Amazon ECR, Ingress NGINX | Production-style three-tier application deployment with persistent storage, Ingress, StatefulSets, ConfigMaps, and Secrets. |

---

# 2-Tier Application

A Kubernetes implementation of a two-tier application consisting of a frontend and backend service deployed on a Kind Kubernetes cluster running on AWS EC2.

## Architecture

```
Internet
    │
MetalLB LoadBalancer
    │
NGINX Frontend
    │
ClusterIP Service
    │
Node.js Backend API
```

## Implemented Features

- Docker containerization for frontend and backend applications
- Kubernetes Deployments for application workloads
- ClusterIP Service for secure backend communication
- LoadBalancer Service using MetalLB
- NGINX Reverse Proxy configuration
- Internal service discovery using Kubernetes DNS
- Container image management using Docker Hub
- Application deployment on Kind Kubernetes cluster hosted on AWS EC2

---

# 3-Tier Application

A production-style Kubernetes deployment consisting of frontend, backend, and MySQL database running on Amazon EKS.

## Architecture

```
Internet
    │
Ingress Controller
    │
Frontend (Flask)
    │
Backend API
    │
MySQL Database
(StatefulSet + PVC)
```

## Implemented Features

- Amazon EKS cluster deployment
- Amazon ECR integration for container images
- Kubernetes Deployments
- Kubernetes StatefulSets
- Persistent Volume Claims (PVC)
- ConfigMaps for application configuration
- Kubernetes Secrets for sensitive credentials
- Namespace-based resource isolation
- Ingress NGINX Controller
- MySQL persistent storage
- Kubernetes Service discovery
- Production-ready application deployment architecture

---

# Technologies Used

| Category | Technologies |
|----------|--------------|
| Containerization | Docker |
| Container Registry | Docker Hub, Amazon ECR |
| Orchestration | Kubernetes |
| Cloud Platform | AWS |
| Kubernetes Platform | Kind, Amazon EKS |
| Networking | Services, Ingress, MetalLB |
| Storage | Persistent Volumes, Persistent Volume Claims |
| Configuration | ConfigMaps, Secrets |
| Database | MySQL |
| Reverse Proxy | NGINX |

---

# Repository Highlights

- End-to-end Kubernetes application deployment
- Multi-tier application architecture
- Production-style Kubernetes resource organization
- Container image management
- Kubernetes networking implementation
- Persistent storage implementation
- Configuration and secret management
- Ingress-based external access
- Namespace-based resource isolation
- Deployment troubleshooting documentation

---

# Prerequisites

Before deploying these projects, ensure the following tools are installed:

- Docker
- kubectl
- Kubernetes Cluster (Kind or Amazon EKS)
- AWS CLI
- Git

---

# Deployment Workflow

1. Clone this repository.
2. Build or pull the required Docker images.
3. Create the required namespaces.
4. Deploy Kubernetes manifests.
5. Verify Pods, Services, and Ingress resources.
6. Access the deployed application.

Detailed deployment instructions are available inside each project directory.

- **2-tier-app/** – Local Kubernetes deployment using Kind
- **3-tier-app/** – Amazon EKS deployment

---

# Repository Structure

```
k8s-deployments
│
├── 2-tier-app
│   ├── frontend
│   ├── backend
│   ├── kubernetes
│   └── README.md
│
├── 3-tier-app
│   ├── frontend
│   ├── backend
│   ├── database
│   ├── kubernetes
│   └── README.md
│
└── README.md
```

---

# Author

**Gorantla Sai Ram**

**AWS DevOps Engineer**

- GitHub: https://github.com/Sairam415
- LinkedIn: https://www.linkedin.com/in/sairamgorantla

---

## ⭐ Support

If you found this repository useful, consider giving it a **Star ⭐**.
