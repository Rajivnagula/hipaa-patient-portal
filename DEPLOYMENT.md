# Deployment Guide

## Prerequisites
- AWS Account with IAM permissions
- Terraform v1.5+
- AWS CLI configured

## Step-by-Step Installation
```bash
# Clone repository
git clone https://github.com/RajJvongulu/hipaa-patient-portal.git
cd hipaa-patient-portal

# Initialize Terraform
terraform init

# Apply configuration (will prompt for variables)
terraform apply

# Verify deployment
terraform output rds_endpoint
