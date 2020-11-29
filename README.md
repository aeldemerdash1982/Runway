# Runway

## Introduction about Runway

Runway is a lightweight wrapper around infrastructure deployment (e.g. CloudFormation, Terraform, Serverless) & linting (e.g. yamllint) tools to ease management of per-environment configs & deployment.

Very simple configuration to:

. Perform automatic linting/verification

. Ensure deployments are only performed when an environment config is present

. Define an IAM role to assume for each deployment

. Wrangle Terraform backend/workspace configs w/ per-environment tfvars

. Avoid long-term tool lock-in

Runway is a simple wrapper around standard tools. It simply helps to avoid convoluted Makefiles / CI jobs

## Use Case

Jenkins is our CICD tool here and we will use github webhook to trigger the build which executes the runway command in SSH shell. The trigger in our case will be any merge to the "Main" branch. We will use CFN module in runway to run the deployment of VPC and servers stacks.

Note: Github replaced Master branch with Main branch recently.

Test


