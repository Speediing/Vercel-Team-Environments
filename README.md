# Vercel Team Environments with Terraform and AWS Secrets Manager

This repository enables structured and secure management of environment variables across multiple teams using Vercel and Terraform, integrating with AWS Secrets Manager.

## Overview

Leverage a modular approach to define and manage environment variables within Vercel projects. This structure enhances clarity and access control, allowing teams to operate independently while maintaining centralized security protocols.

## Structure

- envVariables.tf: Defines the environment variables and assign them to the projects in an individual team.
- projects.tf: Specifies Vercel project configurations.
- secrets.tf: Integrates with AWS Secrets Manager to create/retrieve secret values.
- terraform.tf: The main Terraform configuration file that initializes the provider and sets up the backend.

## Usage

### To use these configurations:

- Ensure you have Terraform installed and AWS CLI configured with the necessary permissions.
- Navigate to the team-specific directory (e.g., team-b).
- Run terraform init to initialize the working directory.
- Configure your AWS Secrets in the AWS Secrets Manager.
- Run terraform plan to see the execution plan and make any necessary adjustments.
- Execute terraform apply to apply the changes to your Vercel environment.

## Security

Secrets are not stored within this repository but are pulled dynamically from AWS Secrets Manager, minimizing the risk of sensitive data exposure.
