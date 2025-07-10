# GCP Secret Manager Infrastructure - Terraform & GitHub Actions

This repository provisions and manages secrets securely in Google Cloud using Infrastructure as Code. It uses Terraform for resource provisioning and GitHub Actions for continuous integration and delivery.

## Overview

This project demonstrates:

- Secure deployment of GCP Secret Manager secrets
- Use of Terraform for declarative infrastructure
- CI/CD automation using GitHub Actions
- Secure handling of secrets and credentials

## Features

- Creates a Secret Manager secret and stores a version (value)
- Uses GitHub Actions to automate `terraform init`, `apply`, and `destroy`
- Uses GitHub Secrets for credential management

## Directory Structure

```
.
├── terraform/
│   ├── main.tf
│   ├── variables.tf
├── .github/workflows/
│   ├── deploy.yml
└── README.md
```

## CI/CD Workflow

### Deployment (`deploy.yml`)

- Manually Triggered
- Initializes Terraform and applies infrastructure
- Pulls credentials from `GCP_CREDENTIALS_JSON` GitHub secret
