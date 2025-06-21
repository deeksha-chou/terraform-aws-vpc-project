# Terraform AWS VPC Web Server Project

This project provisions a basic infrastructure on AWS using Terraform. It sets up a VPC, subnet, internet gateway, route tables, security group, and an EC2 instance configured as a basic Apache web server.

## 🔧 What This Project Does

- Creates a custom **VPC** with CIDR `10.0.0.0/16`
- Adds a **public subnet** in availability zone `us-east-1a`
- Attaches an **Internet Gateway** and associates it with the route table
- Configures a **route table** to allow outbound internet traffic
- Associates the subnet with the route table
- Creates a **security group** allowing traffic on:
  - Port 22 (SSH)
  - Port 80 (HTTP)
  - Port 443 (HTTPS)
- Creates a **network interface** and assigns it a **private IP**
- Allocates an **Elastic IP** and associates it with the network interface
- Launches an **EC2 instance** using an Ubuntu AMI and installs Apache2 with a simple index page

## 🖥️ Technologies Used

- **Terraform** (Infrastructure as Code)
- **AWS EC2, VPC, Subnet, Security Groups, Internet Gateway, Elastic IP**
- **Ubuntu Server**
- **Apache2 Web Server**

## 📁 File Structure
Project 1/
├── main.tf # Main Terraform configuration file
├── variables.tf # (Optional) Variables definition file
├── outputs.tf # (Optional) Outputs for infra
├── .gitignore # Ignoring state files and cache
└── README.md # Project documentation

## 🚀 How to Use This Project

1. **Clone the repo**:
   ```bash
    git clone https://github.com/your-username/terraform-aws-vpc-project.git
    cd terraform-aws-vpc-project
   
2.  **Initialize Terraform:**
    terraform init

3. **Review the plan:**
   terraform plan
   
4.  **Apply the configuration:**
terraform apply

5. **Access your Web Server:**
Once created, copy the Elastic IP from AWS Console and open it in your browser. You should see the message:
your very first web server

🧹 Clean Up
To destroy the infrastructure and avoid charges:
terraform destroy

📌 Prerequisites
AWS CLI configured with valid credentials
Existing AWS Key Pair (e.g., terra-key) in the selected region
Terraform installed locally

✨ Author
Deeksha Choudhary

