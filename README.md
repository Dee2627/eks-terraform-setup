# Production-Grade EKS with Terraform

This repository contains Terraform code to provision a **highly available, production-ready Amazon Elastic Kubernetes Service (EKS) cluster** along with required networking (VPC, Subnets, NAT Gateway, Security Groups, IAM Roles, and Add-ons).

---

## 🚀 Features
- **Modular Terraform setup** (EKS + Networking + IAM roles)
- **S3 Backend with DynamoDB Locking** for remote state management
- **Private + Public Subnets** across multiple Availability Zones
- **EKS Cluster with On-Demand + Spot Node Groups**
- **EKS Add-ons**:
  - VPC CNI
  - CoreDNS
  - Kube-Proxy
  - AWS EBS CSI Driver
- **Security Group** with restricted inbound rules

---

## 📂 Project Structure
Production-EKS-with-Terraform/
│── EKS/ # Main Terraform config for EKS
│ ├── backend.tf # S3 backend for remote state
│ ├── dev.tfvars # Variables for dev environment
│ ├── main.tf # Root module calling sub-modules
│ ├── variables.tf # Input variables
│
│── modules/ # Terraform modules
│ ├── eks.tf # EKS Cluster & Node Groups
│ ├── vpc.tf # VPC, Subnets, Route Tables, NAT
│ ├── iam.tf # IAM Roles & Policies
│ ├── gather.tf # Data sources & OIDC
│ ├── variables.tf # Module variables