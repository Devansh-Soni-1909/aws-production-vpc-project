# aws-production-vpc-project
This project showcases the deployment of a production-grade Virtual Private Cloud (VPC) on Amazon Web Services (AWS), designed with a strong emphasis on high availability, scalability, and security. It simulates a real-world infrastructure environment used by cloud-native applications in production.

# 🚀 Production-Ready VPC on AWS

Super excited to share my latest cloud project — a fully functional Virtual Private Cloud (VPC) that mirrors real-world production-grade infrastructure!

---

## 📘 Project Overview

This project demonstrates how to build a production-grade Virtual Private Cloud (VPC) using AWS. The infrastructure includes high availability, scalability, and secure networking — simulating a real-world backend system setup.

---

## 🗺️ Architecture Diagram

Below is a high-level overview of the infrastructure:
| Architecture Diagram    | ![Architecture Diagram](images/arch.png) |



---

## 🔧 Key Features

- ✅ Multi-AZ EC2 deployment for fault tolerance  
- ✅ Auto Scaling Group (ASG) for dynamic load handling  
- ✅ Application Load Balancer (ALB) for smart routing  
- ✅ Public and Private Subnet separation  
- ✅ NAT Gateways for secure internet access from private subnets  
- ✅ Tight Security Groups and Network ACLs  

---

## ☁️ AWS Services Used

- Amazon VPC  
- EC2 (Elastic Compute Cloud)  
- Auto Scaling Group (ASG)  
- Application Load Balancer (ALB)  
- NAT Gateway  
- Internet Gateway  
- Route Tables  
- Security Groups  
- Network ACLs  

---

## 🛠️ Implementation Steps

1. Created a custom VPC with CIDR block `10.0.0.0/16`  
2. Divided VPC into public and private subnets across 2 AZs  
3. Launched EC2 instances in private subnets  
4. Configured Auto Scaling Group with launch template  
5. Deployed Application Load Balancer in public subnets  
6. Added NAT Gateways to each AZ for outbound internet access from private subnets  
7. Set up route tables, security groups, and health checks  

---

## 🔄 How It Works

- Users access the application via the ALB.  
- ALB routes traffic to healthy EC2 instances in private subnets.  
- ASG monitors load and adjusts EC2 count automatically.  
- NAT Gateway enables backend servers to communicate with the internet (e.g., for updates).  
- All communication is protected using strict security rules.  

---

## 🎯 Why This Matters

- 🔁 **High Availability:** Deploying across multiple AZs increases fault tolerance.  
- 🔐 **Security:** Back-end services are isolated in private subnets.  
- 💰 **Cost-Efficiency:** ASG scales down during low demand.  
- ⚡ **Performance:** Load Balancer ensures smooth user experience.  

---



| Component        | Screenshot        |
|------------------|-------------------|
| VPC Setup        | ![VPC](images/vpc.png) |
| Load Balancer    | ![ALB](images/alb.png) |
| EC2 Instances    | ![EC2](images/ec2.png) |

---

## 📚 What I Learned

- How different AWS networking components interact in a real system  
- Designing fault-tolerant and secure infrastructure  
- Hands-on experience with EC2, ALB, NAT, and ASG  
- Importance of segregating public/private traffic  

---

## 🚀 Future Improvements

- Add a database in private subnets (e.g., RDS or MongoDB)  
- Automate the setup using Terraform or CloudFormation  
- Implement monitoring with CloudWatch and alarms  
- Set up CI/CD pipeline for app deployment  

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 📬 Let's Connect

- 🔗 [LinkedIn](https://linkedin.com/in/devansh-soni)  
- 🐙 [GitHub](https://github.com/Devansh-Soni-1909)

---


