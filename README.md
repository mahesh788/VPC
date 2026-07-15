# VPC
AWS Two-Tier Web Application with Application Load Balancer
**Project Overview**
This project demonstrates the deployment of a highly available two-tier web application on AWS using a custom Virtual Private Cloud (VPC). The infrastructure includes public and private subnets across two Availability Zones, a Bastion Host for secure administration, and an Application Load Balancer to distribute traffic between EC2 instances hosting a Python web application.
## Architecture
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/b1763d28-5e4e-4c9b-8d72-5861fc10e6e5" />

## What I Learned & Implemented
Created a custom Amazon VPC.
Configured Public and Private Subnets across two Availability Zones.
Configured Internet Gateway and NAT Gateway.
Created Route Tables and associated them with subnets.
Launched a Bastion Host in a Public Subnet.
Launched two EC2 instances in Private Subnets.
Configured Security Groups for secure communication.
Connected to private EC2 instances through the Bastion Host using SSH.
Deployed a Python web application on both EC2 instances.
Created an Internet-facing Application Load Balancer.
Configured a Target Group and Health Checks.
Successfully routed application traffic through the Load Balancer.
Verified high availability by ensuring both EC2 instances remained healthy.

## Components Used
Amazon VPC
EC2
Bastion Host
Internet Gateway
NAT Gateway
Route Tables
Security Groups
Application Load Balancer
Target Group
## Outcome
Successfully deployed a Python web application in private EC2 instances and accessed it securely through an Application Load Balancer.
## Learning Outcome
This project improved my understanding of:
AWS Networking
EC2
Load Balancing
High Availability
Cloud Infrastructure

## Practical Implementation

### Step 1: Created AWS Networking
- Created a custom VPC.
- Created 2 Public Subnets.
- Created 2 Private Subnets.
- Attached an Internet Gateway.
- Created a NAT Gateway.
- Configured Route Tables and associated them with the appropriate subnets.
<img width="1445" height="747" alt="image" src="https://github.com/user-attachments/assets/de8e635b-90f0-4d5b-b04c-e6287beed141" />

### Step 2: Launched EC2 Instances
- Launched one Bastion Host in the Public Subnet.
- Launched two EC2 instances in Private Subnets.
- Configured Security Groups for secure communication.
<img width="1650" height="797" alt="image" src="https://github.com/user-attachments/assets/b21d31df-5944-477a-a926-9dcb7aa40e07" />

### Step 3: Connected to Private Instances
- Connected to the Bastion Host using SSH.
- Connected to private EC2 instances from the Bastion Host using a PEM key.
- ssh -i project.pem ubuntu@<Private-EC2-IP>

### Step 4: Deployed Python Application
- Created an index.html file and hosted it using Python.
  **bash**
- python3 -m http.server 8000
- Verified that the application was accessible locally.
  
### Step 5: Configured Application Load Balancer
- Created an Internet-facing Application Load Balancer.
- Created an HTTP Listener on Port 80.
- Created a Target Group.
- Registered both EC2 instances.
- Configured Health Checks on Port 8000.
<img width="1472" height="602" alt="image" src="https://github.com/user-attachments/assets/f0363afb-c7cc-481e-a299-ae0cdfb3dc2b" />

### Step 6: Verified the Deployment
- Confirmed both EC2 instances became **Healthy** in the Target Group.
- Accessed the application using the Application Load Balancer DNS.
- Verified that the application was successfully served through the Load Balancer.
  <img width="1500" height="720" alt="image" src="https://github.com/user-attachments/assets/1e10912a-3246-4328-957e-6d7df088955c" />
  <img width="1596" height="237" alt="image" src="https://github.com/user-attachments/assets/23b71b69-88ae-408b-8e94-d889472d9e8a" />







