# AWS Infrastructure Automation with Terraform

Automate the provisioning of AWS cloud resources and Docker container deployment.

## Tech Stack
- **Infrastructure:** Terraform, AWS
- **Deployment:** Docker, Linux
- **Version Control:** Git

## Infrastructure Components
- **Networking:** VPC, Subnet, Route Table, Internet Gateway
- **Compute:** EC2 Instance
- **Security:** Security Group (Firewall rules)

## Features
- **Infrastructure as Code:** Automated provisioning of a complete VPC environment.
- **Automated Deployment:** Configures EC2 to automatically pull and run a Docker container on launch.

## Modular Version
Refactored infrastructure into reusable modules for scalability:
- **Branch:** `feature/modules`
- **Modules:** `subnet`, `webserver`

## Usage
1. Initialize Terraform: `terraform init`
2. Plan changes: `terraform plan`
3. Apply infrastructure: `terraform apply`
4. Destroy infrastructure: `terraform destroy`
5. Apply infrastructure without approval: `terraform apply -auto-approve`