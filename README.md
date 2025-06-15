# terraform-aws-lambda-ebs-stale-snapshot-cleanup

[![Built with Terraform](https://img.shields.io/badge/Built%20with-Terraform-blue.svg)](https://www.terraform.io/)
[![AWS Lambda](https://img.shields.io/badge/AWS-Lambda-orange.svg)](https://aws.amazon.com/lambda/)
[![Python](https://img.shields.io/badge/Python-3.9-blue.svg)](https://www.python.org/downloads/release/python-390/)

---

## Project Overview

This repository contains a **Terraform** configuration to deploy an **AWS Lambda** function designed for **cost optimization** by automatically identifying and deleting **stale EBS (Elastic Block Store) snapshots**. Stale snapshots are those no longer associated with active EC2 instances or existing volumes.

This project is ideal for understanding how to deploy serverless functions with Infrastructure as Code (IaC) and perform meaningful automated operations in your AWS account.

---

## Architecture

This solution leverages the following AWS services:

* **AWS Lambda:** Executes the Python code responsible for scanning and deleting stale snapshots.
* **AWS IAM (Identity and Access Management):** Provides the necessary permissions for the Lambda function to interact with EC2 (to describe/delete snapshots, volumes, instances) and CloudWatch Logs (for logging function activity).
* **Terraform:** Defines, provisions, and manages all the AWS resources in a declarative and repeatable manner.

In this simplified lab version, the Lambda function is invoked manually for testing. For continuous automation, an EventBridge (CloudWatch Events) schedule would typically be integrated.

---

## Features

* **Automated Stale Snapshot Detection:** Scans for EBS snapshots that meet "stale" criteria.
* **Automated Deletion:** Deletes identified stale snapshots to save storage costs.
* **Serverless:** Runs without managing any servers, scaling automatically as needed.
* **Infrastructure as Code:** Deploys all resources using Terraform for consistent and repeatable setups.
* **Clear Logging:** Integrates with CloudWatch Logs to provide visibility into function execution and deletions.

---

## Prerequisites

Before you begin, ensure you have the following installed and configured:

* **AWS Account:** An active AWS account with programmatic access.
* **Terraform:** [Install Terraform](https://www.terraform.io/downloads.html) (version 1.0+ recommended).
* **AWS CLI (Optional but Recommended):** Configure your AWS credentials using the AWS CLI (`aws configure`) or ensure you can set them via environment variables.

---

## Project Structure

The repository has a simple, logical structure:
```bash
terraform-aws-lambda-ebs-stale-snapshot-cleanup/
├── main.tf                 # The main Terraform configuration file
└── python/
└── lambda_function.py  # The Python code for the Lambda function
```


