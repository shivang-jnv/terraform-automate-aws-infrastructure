# Terraform AWS VPC

A minimalist Terraform project designed to provision a secure Virtual Private Cloud (VPC) and subnet on Amazon Web Services.

## Features

- **Automated Infrastructure**: Quick deployment of VPC and subnets.
- **Configurable**: Easily adjust CIDR blocks and availability zones via variable files.
- **Clear Outputs**: Provides VPC and Subnet IDs for integration with other modules.
- **State Management**: Ready for local or remote state tracking.

## Prerequisites

Before you begin, ensure you have:
- [Terraform](https://www.terraform.io/downloads) installed.
- [AWS CLI](https://aws.amazon.com/cli/) configured with valid credentials.

## Usage

1. **Initialize Terraform**
   ```bash
   terraform init
   ```

2. **Review Infrastructure Plan**
   ```bash
   terraform plan -var-file="terraform-dev.tfvars"
   ```

3. **Deploy Resources**
   ```bash
   terraform apply -var-file="terraform-dev.tfvars"
   ```

> [!TIP]
> Use the `-var-file` flag to maintain different environment configurations (e.g., dev, staging, prod) easily.

## Infrastructure Details

The following resources are managed by this project:
- **VPC**: A development VPC with a customizable CIDR block.
- **Subnet**: A single subnet within the VPC associated with a specific availability zone.

### Variables

| Name | Description |
|------|-------------|
| `cidr_blocks` | List of CIDR blocks for VPC and subnets |
| `avail_zone` | The AWS availability zone to deploy the subnet in |

### Outputs

| Name | Description |
|------|-------------|
| `dev-vpc-id` | The ID of the created VPC |
| `dev-subnet-id` | The ID of the created subnet |
