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
     
<img width="535" alt="image" src="https://github.com/user-attachments/assets/f49727d3-c4e2-4185-bb25-ec9d00713be4" />

3. EC2 Instance Provisioning:
   - Launch two EC2 instances: one in the public subnet (for the web server) and another in the private subnet (for the database).
   - Ensure both instances are accessible via SSH (public instance only accessible from your IP).
All the 3 isntance are launches as shown below 

<img width="535" alt="image" src="https://github.com/user-attachments/assets/759d2f1b-04ed-4061-a44b-2f26b6e22709" />

4. Security Groups and IAM Roles:
   - Create necessary security groups for web and database servers.
   -  created in the terraform script itself 
   - Set up IAM roles for EC2 instances with required permissions.
5. Resource Output:
   - Output the public IP of the web server EC2 instance.

Part 2: Configuration and Deployment with Ansible
   
1. Ansible Configuration:
   - Configure Ansible to communicate with the AWS EC2 instances.
     
Created ansible host file and able to ping to the ec2 instances

![image](https://github.com/user-attachments/assets/0d866a7e-f32c-47e1-8849-17751e3e0995)

2. Web Server Setup:
   - Write an Ansible playbook to install Node.js and NPM on the web server.
   - Clone the MERN application repository and install dependencies.
Created web.yaml and ran it using ansible. It is is able to update the REACT server with all the dependencies.
3. Database Server Setup:
   - Install and configure MongoDB on the database server using Ansible.
   - Secure the MongoDB instance and create necessary users and databases.
Created app.yaml and ran it using ansible. It is is able to update the REACT server with all the dependencies.

4. Application Deployment:
   - Configure environment variables and start the Node.js application.
   - Ensure the React frontend communicates with the Express backend.
  
Application deployment is complete and able to see the following image.

![image](https://github.com/user-attachments/assets/4c738584-a5e5-4bfe-b7fc-7c1d2fb93be3)

![image](https://github.com/user-attachments/assets/55941f49-4954-4b6f-bebc-278a71c15415)

5. Security Hardening:
   - Harden the security by configuring firewalls and security groups.
   - Implement additional security measures as needed (e.g., SSH key pairs, disabling root login).





