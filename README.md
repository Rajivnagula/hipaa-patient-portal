# 🏥 HIPAA-Compliant Patient Portal (AWS)

> **Terraform-managed infrastructure enabling healthcare applications to meet HIPAA technical safeguards §164.312**. Implements encrypted RDS, audit logging, and network isolation while reducing deployment costs by 40% vs manual setups.

## 🔍 Overview
Secure AWS infrastructure solution for processing Protected Health Information (PHI) compliant with HIPAA technical safeguards. Features VPC isolation, KMS encryption, and audit logging to meet §164.312 requirements.

## ✨ Key Features
| **Feature**               | **HIPAA Control**       | **Implementation**               |
|---------------------------|-------------------------|----------------------------------|
| 🔐 Data Encryption       | §164.312(a)(1)          | AES-256 via AWS KMS              |
| 🛡️ Network Isolation     | §164.312(e)(1)          | Public/Private Subnets + NAT     |
| 📜 Audit Logging         | §164.312(b)             | CloudTrail → S3                  |
| 🔑 Access Control        | §164.312(a)(2)(i)       | IAM Least Privilege Policies     |
| 💾 Backup Compliance     | §164.308(a)(7)(ii)(A)   | 35-day Automated Snapshots       |

## ⚙️ Technologies

```mermaid
graph LR
    T["Terraform"] --> A["AWS"]
    A --> V["VPC"]
    A --> R["RDS"]
    A --> K["KMS"]
    A --> I["IAM"]
    A --> C["CloudTrail"]
## 🚀 Deployment

### Prerequisites
- AWS account with admin permissions
- Terraform v1.5+
- AWS CLI configured

### Step-by-Step
```bash
# Clone repository
git clone https://github.com/RajJvongulu/hipaa-patient-portal.git
cd hipaa-patient-portal

# Initialize Terraform
terraform init

# Deploy infrastructure (will prompt for variables)
terraform apply

# Verify deployment
terraform output rds_endpoint
## 👥 Contributors  

<a href="https://github.com/RajJvongulu">
  <img src="https://avatars.githubusercontent.com/u/2118694" width="100" style="border-radius:50%">
</a>

**Sai Rajiv Nagula**  
Lead Cloud Architect  
[![GitHub](https://img.shields.io/badge/GitHub-Profile-blue?logo=github)](https://github.com/RajJvongulu) 
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://linkedin.com/in/sairajiv)  
*MS Information Systems, DePaul University 2025*
