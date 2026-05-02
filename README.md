# Roboshop Deployment on AWS EC2 (Test Project)

This repository demonstrates deploying the **Roboshop microservices application** on an AWS EC2 instance.

The project focuses on understanding cloud fundamentals by manually setting up infrastructure and deploying applications on virtual machines.

---

## Project Overview

Roboshop is a **microservices-based e-commerce application** consisting of services like:

- Web (Frontend)
- Catalogue
- User
- Cart
- Shipping
- Payment
- Dispatch

In this project, the application is deployed directly on an **EC2 instance**, helping to understand how cloud-based servers work.

---

## Tech Stack

- AWS EC2
- Linux (Ubuntu / Amazon Linux)
- Shell Commands / Manual Setup
- Git & GitHub

---

## What is EC2?

Amazon EC2 (Elastic Compute Cloud) is a service that provides virtual servers in the cloud.

It allows you to:

- Launch virtual machines
- Install applications
- Configure networking and security
- Scale infrastructure as needed

---

## Architecture

- EC2 instance acts as the main server
- Roboshop services are installed and run on the instance
- Databases (MongoDB, MySQL, Redis, RabbitMQ) support backend services
- Frontend is accessed via public IP

---

## Setup & Execution

### Launch EC2 Instance

- Choose AMI (Ubuntu / Amazon Linux)
- Select instance type (e.g., `t2.micro` / `t2.medium`)
- Configure security group (allow HTTP/SSH)

---

### Connect to Instance

```bash
ssh ec2-user@<public-ip>
```

---

### Install Dependencies

```bash
sudo yum update -y
sudo yum install git -y
```

---

### Clone Repository

```bash
git clone https://github.com/Jayani22/roboshop-ec2-test.git
cd roboshop-ec2-test
```

---

### Run Setup / Deployment

```bash
chmod +x *.sh
./all.sh
```

*(or run individual service scripts)*

---

## Access Application

Open in browser:

```text
http://<EC2-public-ip>
```

---

## Key Features

- Manual deployment on EC2
- Understanding of cloud infrastructure basics
- Hands-on experience with Linux servers
- Foundation for automation tools (Ansible, Terraform)

---

## Learning Outcomes

Through this project, I gained:

- Experience in launching and managing EC2 instances
- Understanding of cloud networking and security groups
- Hands-on deployment of microservices on cloud
- Troubleshooting real-world deployment issues

---

## Future Enhancements

- Automate setup using Ansible
- Provision infrastructure using Terraform
- Containerize application using Docker
- Deploy using Kubernetes

---

## Note

This project is part of my DevOps learning journey, focusing on understanding cloud fundamentals by deploying applications manually before moving to advanced automation tools.

