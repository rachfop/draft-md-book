# Reference architecture


This repository contains Terraform configurations to deploy a reference architecture on AWS, GCP, and Azure.

The goal of this repository is to provide a starting point for deploying infrastructure on AWS, GCP, and Azure.

The reference architecture includes:

- Virtual Private Cloud (VPC)
- Subnets (public, private, database)
- Route tables
- Kubernetes Engine (EKS, GKE, AKS)
- Node Groups (Auto Scaling Groups, Instance Groups, Node Pools)
- Relational Database Service (RDS, Cloud SQL, Azure Database)
- Object Storage (S3, Google Cloud Storage, Azure Blob Storage)
- Identity and Access Management (IAM, Cloud IAM, Azure Active Directory)

The infrastructure is deployed using Terraform modules to keep the configurations DRY (Don't Repeat Yourself). The modules can be reused and reconfigured as needed to suit your needs.

The repository also includes wrapper modules that call the underlying modules with default configuration to make deployment easy. Just populate the required variables to get started.

This reference architecture can be used as a starting point for your AWS, GCP, and Azure infrastructure needs and built upon as required for your specific use cases. The modules can be used as is or modified to suit your needs.