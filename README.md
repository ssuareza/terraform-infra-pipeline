# terraform-infra-pipeline

This repository is a hands-on example for learning how to set up a pipeline using Terraform, GitHub Actions, and AWS.

It basically creates two S3 buckets:

- `dev-terraform-infra-pipeline`: if you commit changes in a "dev" branch.
- `prod-terraform-infra-pipeline`: if you merge the changes into the main branch through a pull request.

## Requirements

- Terraform v1.3+
- AWS CLI v2

## How to use it?

1. Create a new github repository with this repository code.

2. Connect GitHub Actions to actions in AWS.
<https://aws.amazon.com/blogs/security/use-iam-roles-to-connect-github-actions-to-actions-in-aws/>

3. Create the bucket `ssuareza-terraform-statefile` in AWS S3 to store the terraform statefile.

4. Create a DynamoDB table to store the terraform lockfile.

**Note**: this can be done in S3 as well.

5. Test it by pushing to the "dev" branch. When you're ready to test it in production, just open a pull request and merge your changes.

## Destroy

You can remove all the Terraform created resources by editing "terraform/destroy.json" file. Set the value to "true" and commit your changes.

## Reference

<https://github.com/brunograna/terraform-infra-pipeline>
