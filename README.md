# Ansible
Deploying a MERN Application on AWS

Part 1: Infrastructure Setup with Terraform
1. AWS Setup and Terraform Initialization:
   - Configure AWS CLI and authenticate with your AWS account.
   - Initialize a new Terraform project targeting AWS.
Done using the Terraform script as shown in the GITHUB repository 
2. VPC and Network Configuration:
   - Create an AWS VPC with two subnets: one public and one private.
Done pk1-vpc created with 2 subnets 1 provate and 1 public

<img width="536" alt="image" src="https://github.com/user-attachments/assets/90fc110e-bbe3-464a-b080-38c4e3e70d6d" />

   - Set up an Internet Gateway and a NAT Gateway.
     
<img width="537" alt="image" src="https://github.com/user-attachments/assets/d0b4e455-8120-4e9e-80a7-cd24d78140e9" />

   - Configure route tables for both subnets.
