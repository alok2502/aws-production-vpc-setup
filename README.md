🏗️ AWS Production VPC Setup
This project demonstrates a production-ready VPC architecture on AWS, designed for high availability, scalability, and secure access. It includes a 2-tier infrastructure with public and private subnets, NAT Gateways, Auto Scaling Group (ASG), Application Load Balancer (ALB), and a Bastion Host for SSH access to private instances.

📌 Project Highlights
✅ Multi-AZ Deployment for high availability

🔐 Bastion Host for secure SSH access to private EC2s

🛡️ Private & Public Subnets to isolate resources securely

🔄 Auto Scaling Group (ASG) for automatic scaling

⚖️ Application Load Balancer (ALB) to distribute incoming traffic

🌐 NAT Gateways to allow internet access for private instances

📸 Screenshots and Setup Guides included

Internet
   │
   ▼
[Load Balancer]
   │
   ▼
[Public Subnet AZ1]        [Public Subnet AZ2]
   │                             │
[Bastion Host]             [NAT Gateway]
   │                             │
   └─────────────┐   ┌───────────┘
                 ▼   ▼
        [Private Subnet AZ1]   [Private Subnet AZ2]
                EC2 (App Server via ASG)


✅ Prerequisites:

AWS Account

IAM permissions to create VPC, EC2, ALB, ASG, etc.

Basic knowledge of AWS Networking and EC2

📖 Step-by-Step Flow:

Create a custom VPC across two Availability Zones

Add public and private subnets in both AZs

Configure Internet Gateway and Route Tables

Launch a Bastion Host in the public subnet

Create a NAT Gateway in each public subnet

Launch EC2 instances in private subnets using an Auto Scaling Group

Set up an Application Load Balancer

SSH into private EC2 via Bastion and deploy app

Test traffic distribution through ALB

Monitor EC2 health and scaling behavior

🧠 Lessons Learned
Designed secure and scalable cloud infrastructure

Understood the role of subnets, route tables, NATs, and IGWs

Practiced hands-on auto-scaling and traffic distribution

Improved cloud troubleshooting and architecture design skills

