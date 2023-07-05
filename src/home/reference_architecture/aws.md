# AWS

This repository contains Terraform configurations to deploy a reference architecture on AWS. 

The goal of this repository is to provide a starting point for deploying infrastructure on AWS.

The reference architecture includes:

- VPC
- Subnets (public, private, database)
- Route tables
- EKS Cluster
- Node Groups
- RDS (MySQL)
- S3 Buckets
- IAM Roles and Policies


The infrastructure is deployed using Terraform modules to keep the configurations DRY (Don't Repeat Yourself). The modules can be reused and reconfigured as needed to suit your needs.

The repository also includes wrapper modules that call the underlying modules with default configuration to make deployment easy. Just populate the required variables to get started.

This reference architecture can be used as a starting point for your AWS infrastructure needs and built upon as required for your specific use cases. The modules can be used as is or modified to suit your needs.