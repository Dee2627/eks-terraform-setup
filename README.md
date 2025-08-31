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
