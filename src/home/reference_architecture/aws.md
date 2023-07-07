# AWS

The [Humanitec AWS Reference Architecture](https://github.com/humanitec/reference-architecture-aws) is a set of Terraform configurations that can be used to deploy a reference architecture on AWS.
The Reference Architecture provides a tested and proven architecture that can be used as a starting point. This saves time designing and accelerates deployment, since it provides a common framework and is modular.

## Get started

Get started with the Humanitec AWS Reference Architecture:

1. Clone the repository.

```bash
gh repo clone humanitec/reference-architecture-aws
```

1. Review the variables defined in `variables.tf` files for each build to understand what inputs are required.
   You can provide these variables through one of the following options.
   1. Command line flags when running Terraform a `terraform.tfvars` file in the same directory
   2. Environment variables:
      Choose a build in the builds/ directory to deploy.
      For example, some options are:
      - `aws_static_base`: Deploys core networking infrastructure (VPC, subnets, route tables, etc.)
      - `aws_eks`: Deploys an EKS cluster and node group
      - `aws_rds`: Deploys an RDS database instance
      - `aws_s3`: Deploys an S3 bucket

1. Run `terraform init` to initialize the build.

1. Run `terraform plan` to preview the changes. Review the output to ensure the configuration is correct.

1. Run `terraform apply` to deploy the infrastructure. Enter `yes` when prompted to confirm.

The infrastructure will now deploy. This can take 10-15 minutes for larger builds like `aws_eks`.

Once deployed, you can view your AWS resources in the AWS Console and begin using services like EKS, RDS, and S3.

When no longer needed, run `terraform destroy` to tear down the infrastructure.

This will get you started with deploying the reference architecture.
