# terraform-infra-pipeline

## Requirements

- Terraform v1.3+
- AWS CLI v2

## How to use it?

1. Create an Indentiy Provider in AWS IAM.

2. Create a bucket to store the terraform statefile.

3. Create a dynamodb table to store terraform lockfile.

4. Set your AWS credentials:
