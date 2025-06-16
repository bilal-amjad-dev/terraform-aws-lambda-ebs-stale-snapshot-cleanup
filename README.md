# terraform-aws-lambda-ebs-stale-snapshot-cleanup

[![Built with Terraform](https://img.shields.io/badge/Built%20with-Terraform-blue.svg)](https://www.terraform.io/)
[![AWS Lambda](https://img.shields.io/badge/AWS-Lambda-orange.svg)](https://aws.amazon.com/lambda/)
[![Python](https://img.shields.io/badge/Python-3.9-blue.svg)](https://www.python.org/downloads/release/python-390/)

---

![Image](https://github.com/user-attachments/assets/0c21c025-c76c-4dca-abfe-ea97575f4510)



## Prerequisites

Before you begin, ensure you have the following installed and configured:

* **AWS Account:** An active AWS account with programmatic access.
* **Terraform:** [Install Terraform](https://www.terraform.io/downloads.html) (version 1.0+ recommended).
* **Code Editor:** VS Code (Recommednded) 


## Project Structure

The repository has a simple, logical structure:
```bash
terraform-aws-lambda-ebs-stale-snapshot-cleanup/
├── main.tf                 # The main Terraform configuration file
└── python/
└── lambda_function.py  # The Python code for the Lambda function
```
```bash
terraform init
terraform plan
terraform apply
```
```bash
terraform destroy
```

