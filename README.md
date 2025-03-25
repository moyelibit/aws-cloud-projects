# AWS EC2 Ubuntu Server Deployment

This project demonstrates how to launch, configure, and manage an Ubuntu Server virtual machine using Amazon EC2.

## 📌 Objective

Deploy a secure and functional Ubuntu Server instance in the AWS cloud as part of a cybersecurity course project, focusing on VM provisioning and hands-on cloud infrastructure experience.

## 🛠️ Technologies Used

- Amazon EC2 (Elastic Compute Cloud)
- Ubuntu Server 64-bit
- SSH (Secure Shell)
- AWS Security Groups
- Key Pair Authentication

## 🔧 Project Steps

1. **Log into AWS Console**
   - Navigate to EC2 dashboard.
   - Click “Launch Instance”.

2. **Configure the Virtual Machine**
   - Select **Ubuntu Server 64-bit** as the Amazon Machine Image (AMI).
   - Choose **t2.micro** instance type (Free Tier eligible).
   - Create or select an existing **key pair** for secure SSH access.

3. **Set Up Networking**
   - Configure a **security group** to allow SSH (port 22).
   - Restrict SSH access to your public IP address.

4. **Launch the Instance**
   - Review and launch the instance.
   - Download the `.pem` key file if creating a new key.

5. **Connect to Ubuntu Server**
   - Use SSH to connect:
     ```bash
     chmod 400 your-key.pem
     ssh -i your-key.pem ubuntu@<your-public-ec2-ip>
     ```

6. **Post-Deployment Tasks**
   - Update the system:
     ```bash
     sudo apt update && sudo apt upgrade -y
     ```
   - Install additional tools as needed (e.g., Nginx, fail2ban, ufw).

7. **Shutdown and Clean Up**
   - Stop and terminate the EC2 instance when the project is complete to avoid charges.

## 🖼️ Screenshots

> (Add your screenshots here showing the instance running, the terminal connection, and any configurations.)

## ✅ Outcome

Successfully deployed and managed a cloud-based Ubuntu Server, demonstrating the ability to:
- Configure secure virtual machines
- Navigate AWS EC2 services
- Apply cybersecurity best practices in cloud environments

## 🧠 What I Learned

- Hands-on EC2 provisioning
- Key pair and SSH-based secure access
- Networking and firewall configuration in AWS
- Ubuntu system updates and security practices
