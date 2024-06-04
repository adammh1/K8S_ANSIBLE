# Overview
This repository contains GitHub Actions workflows for building, analyzing, and deploying a Node.js application. The workflows are triggered on pushes to the main and EKS branches.

# Workflow Details
## Main Branch Workflow
- Steps:
1.  Checkout code
2. SonarQube analysis
3. Disable warnings as errors
4. Get application version
5. Setup Node.js
6. Install dependencies and build
7. Build artifact
8. Publish to Nexus
9. Configure AWS credentials
10. Login to Amazon ECR
11. Build and push Docker image
12. Create Kubernetes namespace
13. Deploy to local Kubernetes cluster
## EKS Branch Workflow
- Steps:
1. Checkout code
2. SonarQube analysis
3. Disable warnings as errors
4. Get application version
5. Setup Node.js
6. Install dependencies and build
7. Build artifact
8. Publish to Nexus
9. Configure AWS credentials
10. Login to Amazon ECR
11. Build and push Docker image
12. Get kubeconfig file
13. Create Kubernetes namespace
14. Deploy to EKS cluster
# Required Secrets
- SONARQUBE_TOKEN
- SONAR_HOST_URL
- NEXUS_REPO
- NEXUS_USERNAME
- NEXUS_PASSWORD
- AWS_ACCOUNT_ID
- LOCAL_CONTEXT (for main branch)
- EKS_CONTEXT (for EKS branch)