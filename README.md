# Automated AWS Web Infrastructure Deployment using Terraform

Terraform-based AWS infrastructure project that provisions a highly available web application using EC2 instances behind an Application Load Balancer, demonstrating Infrastructure as Code, automated provisioning, and cloud networking.

## Overview

This project demonstrates how to provision a highly available web infrastructure on AWS using **Terraform Infrastructure as Code (IaC)**.

The infrastructure deploys multiple EC2 web servers across different Availability Zones and exposes them through an **Application Load Balancer (ALB)** to ensure high availability, scalability, and fault tolerance.

The entire environment is provisioned automatically using Terraform, eliminating the need for manual configuration in the AWS console.

---

## Problem Statement

In traditional infrastructure setups, provisioning servers and configuring networking resources manually can lead to:

* Human errors during configuration
* Lack of scalability
* Difficult infrastructure replication
* Inconsistent environments across deployments

Organizations require an automated approach to **provision and manage infrastructure reliably and consistently**.

This project solves the problem by using **Infrastructure as Code (IaC)** with Terraform to automatically provision a scalable and highly available AWS environment.

---

## Solution Architecture

The Terraform configuration provisions the following AWS resources:

* Custom **Virtual Private Cloud (VPC)**
* **Public Subnets** across multiple Availability Zones
* **Internet Gateway** for internet connectivity
* **Route Tables** for network routing
* **Security Groups** for controlled inbound and outbound access
* **Two EC2 Instances** running Apache Web Server
* **Application Load Balancer (ALB)** for distributing traffic
* **Target Group with Health Checks**

The Application Load Balancer distributes incoming traffic between the EC2 instances to ensure continuous service availability.

---

## Architecture Diagram (Logical Flow)

Internet
│
▼
Application Load Balancer
│
├── EC2 Instance (Subnet 1 - AZ1)
│       Apache Web Server
│
└── EC2 Instance (Subnet 2 - AZ2)
        Apache Web Server

---

## Key Features

* Fully automated infrastructure provisioning using **Terraform**
* High availability using **multiple Availability Zones**
* Traffic distribution with **AWS Application Load Balancer**
* **Health checks** to detect unhealthy instances
* Dynamic web page displaying **EC2 Instance ID**
* Infrastructure reproducibility and version control

---

## Technologies Used

* **Terraform**
* **AWS EC2**
* **AWS VPC**
* **AWS Application Load Balancer**
* **AWS Security Groups**
* **Linux (Apache Web Server)**
* **Bash scripting**

---

## Infrastructure as Code Concepts Demonstrated

This project demonstrates the following Terraform concepts:

* Resource provisioning
* Dependency management
* Modular infrastructure design
* Automated provisioning
* Output variables
* User data bootstrapping

---

## How to Deploy

1. Clone the repository

```bash
git clone https://github.com/yourusername/terraform-aws-alb-project.git
cd terraform-aws-alb-project
```

2. Initialize Terraform

```bash
terraform init
```

3. Review the infrastructure plan

```bash
terraform plan
```

4. Deploy the infrastructure

```bash
terraform apply
```

5. Access the application

After deployment, Terraform outputs the **Application Load Balancer DNS name**.

Open it in your browser:

```
http://<ALB-DNS>
```

Refreshing the page will show different **EC2 Instance IDs**, proving that load balancing is working.

---

## Learning Outcomes

Through this project, the following DevOps and Cloud engineering skills were demonstrated:

* Designing cloud infrastructure using **Infrastructure as Code**
* Implementing **high availability architecture**
* Automating server configuration using **EC2 User Data scripts**
* Configuring **AWS networking components**
* Implementing **load balancing and health checks**
* Managing infrastructure lifecycle using Terraform

---


## Why This Project Matters

This project demonstrates the ability to:

* Design scalable cloud infrastructure
* Automate deployments using Terraform
* Implement high availability architectures on AWS
* Apply DevOps best practices in real-world scenarios

