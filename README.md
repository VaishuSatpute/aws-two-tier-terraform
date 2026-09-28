# AWS Two-Tier Infrastructure with Terraform

A Terraform practice project for provisioning a secure two-tier AWS architecture using reusable infrastructure-as-code concepts.

## Architecture

**Internet → CloudFront / Route 53 / WAF → ALB → EC2 Auto Scaling → RDS**

Supporting services can include:

- Amazon VPC
- Public/private subnets
- IAM
- WAF
- Application Load Balancer
- Auto Scaling Group
- EC2
- RDS
- S3
- CloudFront
- Route 53
- ACM

## Terraform Concepts

- Providers
- Variables
- Outputs
- Modules
- Resource dependencies
- Terraform plan/apply/destroy
- Modular infrastructure design
- Sensitive configuration handling

## Typical Workflow

```bash
terraform init
terraform validate
terraform plan -var-file=variables.tfvars
terraform apply -var-file=variables.tfvars
```

To remove resources:

```bash
terraform destroy -var-file=variables.tfvars
```

## Security Notes

Credentials and passwords should be supplied through secure variables or secret-management mechanisms and should never be committed to Git.

## Deployment Status

This is an infrastructure-as-code learning/practice repository. No AWS deployment is claimed because the infrastructure has not been applied to a live AWS account.

## Source / Attribution

The architecture and learning material were studied from the DevOps-Projects community repository and adapted for practice.