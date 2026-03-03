Hands-on AWS project focused on networking, security, and layered architecture design.
# AWS WordPress 2-Tier Architecture

## 📌 Project Overview
This project demonstrates a 2-tier architecture deployed on AWS.

The goal is to build a secure and structured environment by separating the web server and database server into different subnets within a custom VPC.

## 🏗 Architecture Design

- Custom VPC
- 2 Availability Zones
- Public Subnet (Web Layer)
- Private Subnet (Database Layer)
- Internet Gateway
- Route Tables
- 2 Separate Security Groups
- EC2 (WordPress)
- EC2 (MariaDB)

## ⚙️ Implementation Details

### 🌐 Web Layer (Public Subnet)
- EC2 instance deployed in Public Subnet
- WordPress installed and configured
- Security Group allows:
  - HTTP (80) from 0.0.0.0/0
  - HTTPS (443) from 0.0.0.0/0
  - SSH (22) from trusted IP

### 🛢 Database Layer (Private Subnet)
- EC2 instance deployed in Private Subnet
- MariaDB installed
- Security Group allows:
  - MySQL (3306) only from Web Server Security Group

## 🔐 Security Approach
- Database server is not publicly accessible
- Layered architecture (Web + DB separation)
- Security Groups used for controlled communication between tiers
- Public and Private subnet isolation

## 📷 Architecture Diagram
(Add your architecture.png image here)

## 🚀 Future Improvements
- Application Load Balancer
- Auto Scaling Group
- RDS instead of EC2-based database
- NAT Gateway for private subnet outbound access
- Infrastructure as Code (Terraform)
- CI/CD integration

## 🎯 Learning Outcomes
Through this project, I practiced:
- AWS VPC networking fundamentals
- Public vs Private subnet design
- Security Group configuration
- Basic cloud architecture design principles
