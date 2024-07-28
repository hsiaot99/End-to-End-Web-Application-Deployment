# End-to-End-Web-Application-Deployment

## Overview
This repository contains Terraform configurations for deploying a fully-functional web application infrastructure on AWS. The setup includes the following components:
- **VPC (Virtual Private Cloud)**: Provides a secure network environment for your application.
- **RDS (Relational Database Service)**: Managed database service with replication.
- **Web Server (NGINX)**: Hosted on EC2 instances, managed with auto-scaling and load balancing.

### Components
1. **RDS (Relational Database Service)**
   - **Primary DB**: A managed MySQL database instance with replication enabled.
   - **Replication**: Configured for high availability and failover.
2. **Auto Scaling Group and Launch Configuration**
   - **Auto Scaling Group**: Ensures that the number of EC2 instances adjusts automatically based on demand.
   - **Launch Configuration**: Defines the configuration for new EC2 instances, including AMI, instance type, and user data.
3. **Load Balancers**
   - **Application Load Balancer (ALB)**: Distributes incoming traffic across multiple EC2 instances.
4. **EC2 Instance for Web Server**
   - **NGINX**: Web server running on EC2 instances, serving static content and load-balanced traffic.
5. **Security Groups**
   - **For Each Resource**: Configures network access rules for RDS, EC2 instances, and load balancers.
6. **VPC (Virtual Private Cloud)**
   - **Network Isolation**: Custom VPC with public and private subnets.
   - **Internet Gateway and NAT Gateway**: Facilitates internet access for public resources and private subnet access.
Ref. https://www.udemy.com/course/terraform_training/
