# AWS EKS Cluster Setup with Ansible
This repository contains an Ansible playbook to automate the creation of AWS resources and the setup of an EKS (Elastic Kubernetes Service) cluster.

# Playbook Overview
AWS Resources Creation and EKS Cluster Setup: The playbook AWS_EKS_Setup.yaml creates a VPC, subnets, an Internet Gateway, a Security Group, an EKS cluster, and worker nodes. It also updates the kubeconfig and creates an ECR (Elastic Container Registry) repository.
# Prerequisites
Before running this playbook, ensure you have the following:

- Ansible installed on your control machine.
- AWS CLI installed and configured with the necessary permissions.
- IAM roles for EKS and worker nodes created in AWS.