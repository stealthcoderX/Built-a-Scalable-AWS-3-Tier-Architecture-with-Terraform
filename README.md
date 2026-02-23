# 🚀 Built a Scalable AWS 3-Tier Architecture with Terraform

> Infrastructure as Code project demonstrating a production-style highly available 3-tier architecture on AWS using Terraform.

---

## 📌 Project Overview

This project provisions a *fully scalable and secure 3-tier architecture* in AWS using Terraform.

The infrastructure follows industry best practices:

- Separation of Web, Application, and Database layers
- Public and Private subnet isolation
- Load balancing and Auto Scaling
- Secure networking using Security Groups and NAT Gateway
- Infrastructure fully automated using Terraform

This project demonstrates real-world DevOps and Cloud Engineering skills including infrastructure design, networking, scalability, and automation.

---

## 🏗 Architecture Diagram
Internet
                        │
                        ▼
             ┌────────────────────┐
             │ Application Load   │
             │     Balancer       │
             │     (Public)       │
             └────────────────────┘
                        │
                        ▼
            ┌──────────────────────┐
            │   Web Tier (EC2)     │
            │  Auto Scaling Group  │
            │   Public Subnets     │
            └──────────────────────┘
                        │
                        ▼
            ┌──────────────────────┐
            │ Application Tier EC2 │
            │  Auto Scaling Group  │
            │   Private Subnets    │
            └──────────────────────┘
                        │
                        ▼
            ┌──────────────────────┐
            │     Database Tier    │
            │      (Private)       │
            │        MySQL         │
            └──────────────────────┘
Copy code

---

## 🧱 Architecture Components

### 🌐 Networking Layer
- Custom VPC
- Public Subnets (Web Tier)
- Private Subnets (App + DB Tier)
- Internet Gateway
- NAT Gateway
- Route Tables

### ⚖ Load Balancing
- Application Load Balancer (ALB)
- Target Groups
- Health Checks

### 🖥 Compute Layer
- EC2 Instances
- Launch Template
- Auto Scaling Group

### 🔐 Security
- Security Groups
- Public/Private Network Isolation
- Controlled Inbound & Outbound Rules

### 💾 Data Layer
- MySQL Database (Private Network)

---

## 📂 Repository Structure
. ├── provider.tf ├── variables.tf ├── vpc.tf ├── subnet.tf ├── internetgw.tf ├── natgw.tf ├── route_table.tf ├── sg.tf ├── ec2.tf ├── alb.tf ├── outputs.tf
Copy code

Each file is modularized to maintain clean Infrastructure as Code practices.

---

## 🛠 Prerequisites

Before deploying, ensure you have:

- AWS Account
- AWS CLI configured (aws configure)
- Terraform installed (v1.5+ recommended)
- Proper IAM permissions to create:
  - EC2
  - VPC
  - ALB
  - Auto Scaling
  - IAM Roles

---

## 🚀 Deployment Steps

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/stealthcoderX/Built-a-Scalable-AWS-3-Tier-Architecture-with-Terraform.git
cd Built-a-Scalable-AWS-3-Tier-Architecture-with-Terraform
2️⃣ Initialize Terraform
Bash
Copy code
terraform init
3️⃣ Validate Configuration
Bash
Copy code
terraform validate
4️⃣ Plan Deployment
Bash
Copy code
terraform plan
5️⃣ Apply Infrastructure
Bash
Copy code
terraform apply
Type yes when prompted.
📤 Outputs
After successful deployment, Terraform will output:
VPC ID
Subnet IDs
ALB DNS Name
EC2 Instance IDs
You can access the application using the ALB DNS endpoint.
🔄 Destroy Infrastructure
To avoid AWS charges:
Bash
Copy code
terraform destroy
📈 Scalability Features
Auto Scaling automatically adjusts instances based on load
ALB distributes traffic across healthy instances
NAT Gateway allows private resources internet access securely
Multi-subnet deployment improves availability
🔐 Security Best Practices Implemented
Database placed in private subnet
Application servers isolated from public internet
Least privilege networking rules
No direct database public exposure
💰 Cost Consideration
Resources like:
NAT Gateway
EC2 Instances
ALB
RDS (if used)
may incur AWS charges. Always run terraform destroy after testing.
📚 Skills Demonstrated
AWS Networking
Infrastructure as Code (Terraform)
High Availability Architecture
Auto Scaling
Load Balancing
DevOps Best Practices
🎯 Future Improvements
Remote Backend (S3 + DynamoDB)
CI/CD Integration using GitHub Actions
Monitoring with CloudWatch
HTTPS using ACM Certificate
WAF Integration
👨‍💻 Author
stealthcoderX
Cloud & DevOps Enthusiast
Building scalable cloud infrastructure projects.
📄 License
This project is open-source and available under the MIT License.
Copy code

---

If you want, I can now:

- 🔥 Upgrade this to *“Interview-Level Documentation”*
- 📊 Add *Mermaid Architecture Diagram*
- ⚙ Add *GitHub Actions CI/CD workflow*
- 🧠 Add *Terraform Remote Backend configuration*
- 📄 Make it more recruiter-optimized**
