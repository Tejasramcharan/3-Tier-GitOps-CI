# 3-Tier GitOps CI/CD Pipeline on AWS EKS

<img width="1472" height="1640" alt="image" src="https://github.com/user-attachments/assets/eb56bd70-c66f-4347-8e21-35abb363e329" />


##  Project Overview

This project demonstrates an **end-to-end enterprise-grade DevOps implementation** for deploying a **3-tier application** using modern CI/CD and GitOps practices.

It showcases how infrastructure, application delivery, and deployment automation can be fully managed using cloud-native DevOps tools.

This implementation includes:

- Infrastructure provisioning using **Terraform**
- Containerized application deployment using **Docker**
- Automated CI pipeline using **GitHub Actions**
- Image publishing to **Docker Hub**
- GitOps-based Continuous Delivery using **ArgoCD**
- Deployment to **Amazon EKS (Kubernetes)**

---

## 🏗 Architecture

### High-Level Architecture Flow

Developer pushes code → GitHub Actions triggers CI → Docker image build → Push image to Docker Hub → GitOps CD repository updated → ArgoCD detects manifest changes → Sync deployment to EKS cluster → Application goes live.

---

##  Architecture Components

### Infrastructure Layer
Provisioned using Terraform:

- AWS VPC
- Public & Private Subnets
- Internet Gateway
- Route Tables
- Security Groups
- IAM Roles
- Amazon EKS Cluster
- EC2 Instance (Management / Bastion Host)

---

### CI Layer (Continuous Integration)

Repository:
**CI Repository:** https://github.com/Tejasramcharan/3-Tier-GitOps-CI

GitHub Actions pipeline handles:

- Source Code Checkout
- Build Process
- Docker Image Creation
- Docker Image Tagging
- Push to Docker Hub

CI Tools:

- GitHub Actions
- Docker
- Docker Hub

---

### CD Layer (GitOps Continuous Delivery)

Repository:
 **CD Repository:** https://github.com/Tejasramcharan/3-Tier-GitOps-CD

ArgoCD continuously monitors Kubernetes manifests in the GitOps repository.

When image tags or deployment configs change:

- ArgoCD detects updates
- Automatically syncs manifests
- Deploys changes into EKS
- Maintains desired cluster state
- Self-heals drift automatically

CD Tools:

- ArgoCD
- Kubernetes
- GitOps

---

## Tech Stack

| Category | Tools |
|--------|------|
| Cloud | AWS EC2, AWS EKS |
| Infrastructure as Code | Terraform |
| CI/CD | GitHub Actions, ArgoCD |
| Containerization | Docker |
| Container Registry | Docker Hub |
| Orchestration | Kubernetes |
| GitOps | ArgoCD |
| Version Control | GitHub |

---

## CI/CD Workflow

### Step 1 — Code Commit
Developer pushes application code to GitHub.

### Step 2 — CI Pipeline Trigger
GitHub Actions automatically triggers pipeline execution.

### Step 3 — Build & Containerization
Application is built and packaged into a Docker image.

### Step 4 — Push to Registry
Docker image is pushed to Docker Hub.

### Step 5 — GitOps Update
Deployment manifests in CD repository are updated.

### Step 6 — ArgoCD Sync
ArgoCD detects manifest changes.

### Step 7 — Kubernetes Deployment
ArgoCD deploys updated application into Amazon EKS.

### Step 8 — Production Live
Application becomes accessible to end users.

---

##  Key DevOps Concepts Demonstrated

 Infrastructure as Code (IaC)  
 CI/CD Automation  
 GitOps Workflow  
 Kubernetes Deployment Automation  
 Cloud Infrastructure Provisioning  
 Containerized Application Delivery  
 Declarative Deployment Management  
 Automated Continuous Delivery  
 Self-Healing Infrastructure  

---

##  Why This Project Matters

This project demonstrates practical experience with enterprise DevOps workflows including:

- Real-world CI/CD implementation
- GitOps deployment strategy
- Kubernetes production workflows
- AWS infrastructure automation
- Scalable cloud-native deployment architecture

This is aligned with modern DevOps/SRE engineering practices used in production environments.

---

##  Repository Structure

### CI Repository
Handles CI automation pipeline.

🔗 https://github.com/Tejasramcharan/3-Tier-GitOps-CI

---

### CD Repository
Handles GitOps deployment manifests and ArgoCD delivery.

🔗 https://github.com/Tejasramcharan/3-Tier-GitOps-CD

---

## Future Enhancements

Planned improvements:

- Prometheus Monitoring
- Grafana Dashboards
- Loki Log Aggregation
- Trivy Security Scanning
- SonarQube Code Quality Analysis
- Slack Notifications
- Blue-Green Deployment
- Canary Releases

---

##  Author

**Tejas Ramcharan**

DevOps Engineer | AWS | Kubernetes | Terraform | GitOps | CI/CD
