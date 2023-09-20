# Sidecar - Terraform AWS EC2

A quick start to deploy a sidecar to AWS EC2 using Terraform!

## Architecture

![Deployment architecture](images/aws_architecture.png)

## Deployment

The elements shown in the [architecture diagram](#architecture) are deployed by the [Cyral Sidecar module for AWS EC2](https://registry.terraform.io/modules/cyralinc/sidecar-ec2/aws/latest). The module requires existing VPC and subnets in order to create the necessary components for the sidecar to run. In a high-level, these are the resources deployed:

* EC2
    * Auto scaling group (responsible for deploying the EC2 instances)
    * Network load balancer
    * Security group
* AWS Secrets Manager
    * Sidecar credentials (optionally created)
    * Sidecar CA certificate
    * Sidecar self-signed certificate
* AWS Cloudwatch
    * Log group (optionally created)

### Requirements




[AWS Provider](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)
[Cyral Sidecar module for AWS EC2](https://registry.terraform.io/modules/cyralinc/sidecar-ec2/aws/latest)

[Terraform](https://www.terraform.io)
[Terragrunt](https://terragrunt.gruntwork.io/)

what tools are needed and min version if required, if none are needed remove this section

### Examples

#### Quickstart
this should show how to deploy with minimal configuration or requirements to get a user going as quickly as possible

#### Production Starting Point

### Parameters

| Name | Default Value | Description |
| --- | --- | --- |
| `x` | `x` | x |

## Limitations
provide any limitations, known issues, unsupported configurations
