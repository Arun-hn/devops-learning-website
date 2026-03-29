# Terraform Infrastructure as Code Guide

## Introduction to Terraform
Terraform is an open-source infrastructure as code software tool created by HashiCorp. It allows you to define your infrastructure using a high-level configuration language, known as HashiCorp Configuration Language (HCL), or JSON.

## Setting Up Terraform Modules
Modules are containers for multiple resources that are used together. A module can call other modules, which allows for reuse and organization of code. 

### Creating a Module
1. Create a directory for your module.
2. Create a `main.tf` file inside that directory.
3. Define your resources in the `main.tf` file.

Example:
```hcl
# main.tf

provider "aws" {
  region = "us-west-2"
}

resource "aws_s3_bucket" "my_bucket" {
  bucket = "my-unique-bucket-name"
  acl    = "private"
}
```

### Using a Module
You can use a module by calling it in your root module.

Example:
```hcl
module "s3_bucket" {
  source = "./modules/s3"
}
```

## State Management
Terraform maintains a state file (`terraform.tfstate`) to map real-world resources to your configuration.

### Key Points:
- The state file is crucial for Terraform to understand the resources it manages.
- You should configure remote state storage in production environments (e.g., AWS S3, Azure Blob Storage).
  
Example (remote state in S3):
```hcl
tf{
  backend "s3" {
    bucket         = "my-terraform-state-bucket"
    key            = "terraform/state"
    region         = "us-west-2"
  }
}
```

## Real-World Examples
1. **EC2 Instance Deployment**:
   ```hcl
   resource "aws_instance" "app_server" {
     ami           = "ami-123456"
     instance_type = "t2.micro"
   }
   ```

2. **VPC Creation**:
   ```hcl
   resource "aws_vpc" "main" {
     cidr_block = "10.0.0.0/16"
   }
   ```

This guide serves as an introductory resource to get started with Terraform, focusing on essential concepts and real-world applications.