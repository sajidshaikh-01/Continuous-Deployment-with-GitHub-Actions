# 🚀 Production-Ready CI/CD Pipeline with GitHub Actions, ArgoCD & EKS

This repository demonstrates a **complete CI/CD workflow** for a containerized application deployed on **Amazon EKS (Elastic Kubernetes Service)** using **GitHub Actions** for automation and **ArgoCD** for GitOps-based Continuous Deployment.

---

## 🧩 Architecture Overview


### ⚙️ CI/CD Flow
1. **CI Pipeline**
   - Triggered when code is pushed to the `main` branch.
   - Builds a Docker image.
   - Pushes the image to Docker Hub (or any registry).
   - Updates the Kubernetes manifests with the new image tag.

2. **CD Pipeline**
   - Triggered automatically after the CI pipeline completes.
   - Connects to **ArgoCD** using CLI and credentials.
   - Syncs the ArgoCD application with the latest manifests.
   - Deploys the new version to **EKS** automatically.

---

GitHub Secrets Required
Secret Name	Description
DOCKERHUB_USERNAME	Docker Hub username
DOCKERHUB_TOKEN	Docker Hub access token
ARGOCD_SERVER	ArgoCD API endpoint (e.g. argocd.example.com)
ARGOCD_USERNAME	ArgoCD login username
ARGOCD_PASSWORD	ArgoCD login password or API token

