# AWS-Infrastructure-with-Terraform-EC2-S3-DynamoDB-
This repository contains the Terraform configuration files to provision a foundational AWS infrastructure consisting of an Amazon EC2 instance, an S3 bucket, and a DynamoDB table.


## Architecture Overview

*   **Amazon EC2:** Provisions a virtual server (e.g., Ubuntu/Amazon Linux) with specified security groups for SSH and web traffic access.
*   **Amazon S3:** Creates a secure, private bucket for object storage (ideal for application assets or remote state storage).
*   **Amazon DynamoDB:** Sets up a managed NoSQL database table with a defined primary key.

---

## Prerequisites

Before deploying, ensure you have the following installed and configured:

1.  **Terraform:** Installed on your local machine ([Download here](https://developer.hashicorp.com/terraform/downloads)).
2.  **AWS CLI:** Installed and configured with your AWS credentials (`aws configure`).
3.  **IAM Permissions:** The AWS user must have permissions to manage EC2, S3, and DynamoDB resources.

---
📂 Project Structure
├── main.tf              # Core resource definitions (EC2, S3, DynamoDB)
├── providers.tf         # AWS provider configurations
├── variables.tf         # Input variables (AWS Region, Instance Types)
├── outputs.tf           # Resource outputs (EC2 Public IP, S3 Bucket Name)
└── .gitignore           # Prevents local tracking of state and sensitive data
