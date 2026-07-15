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
-Amazon VPC
-EC2
-Bastion Host
-Internet Gateway
-NAT Gateway
-Route Tables
-Security Groups
-Application Load Balancer
-Target Group

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




