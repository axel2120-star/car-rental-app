# 🚗 Car Rental Application - DevOps Project

## 📌 Overview
This project demonstrates an end-to-end deployment of a Car Rental Application using modern DevOps tools and practices on AWS.

The application is containerized using Docker and deployed on a Kubernetes cluster (Amazon EKS), with infrastructure provisioned using Terraform.

---

## 🏗️ Architecture

User → ALB → Ingress → Kubernetes Services → Pods → RDS Database

---

## ⚙️ Tech Stack

- **Cloud**: AWS (EKS, ECR, RDS, VPC, ALB)
- **Infrastructure as Code**: Terraform
- **Containerization**: Docker
- **Orchestration**: Kubernetes
- **CI/CD**: GitHub Actions
- **Monitoring**: Prometheus & Grafana

---

## 📁 Project Structure
car-rental-devops/
│
├── terraform/
│ ├── vpc.tf
│ ├── eks.tf
│ ├── rds.tf
│ ├── variables.tf
│
├── app/
│ ├── frontend/
│ ├── backend/
│
├── k8s/
│ ├── deployment.yaml
│ ├── service.yaml
│ ├── ingress.yaml


---

## 🚀 Deployment Steps

### 1. Clone Repository
```bash
git clone https://github.com/YOUR_USERNAME/car-rental-app.git
cd car-rental-app

cd terraform
terraform init
terraform apply

aws eks update-kubeconfig --region ap-south-1 --name car-rental-eks
kubectl get nodes

4. Deploy Application
kubectl apply -f k8s/

🔄 CI/CD Pipeline
Triggered on every push to main
Builds Docker image
Pushes to AWS ECR
Deploys to EKS automatically
📊 Monitoring
Prometheus for metrics collection
Grafana for visualization dashboards
🔐 Security Best Practices
IAM roles for EKS
Private subnets for worker nodes
Secure database using RDS
Secrets management (recommended improvement)
💡 Future Improvements
Helm charts for deployment
HTTPS with ACM & Route53
Autoscaling using HPA
Microservices architecture
📬 Contact

If you like this project or want to collaborate:

LinkedIn: https://linkedin.com/in/https://www.linkedin.com/in/mohammad-afrid-87002223b/
GitHub: https://github.com/axel2120-star
