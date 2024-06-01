# Kubernetes Cluster Setup with Ansible
This repository contains Ansible playbooks to set up a Kubernetes cluster. The setup is divided into multiple stages, each handled by a separate playbook.

## Playbooks Overview
1. 0-InstallTools.yaml: 
Installs the necessary prerequisites for setting up Kubernetes, including Docker and other essential tools.
2. 1-KubeInit.yaml: Initializes the Kubernetes master node using kubeadm.
3. 2-PodNetwork.yaml: Configures the pod network for the Kubernetes cluster.
## Prerequisites
Before running these playbooks, ensure you have the following:

## Ansible installed on your control machine.
- SSH access to the target machines with root privileges.
- A supported version of Ubuntu (e.g., 20.04) on the target machines.
## Usage

1. **Update the inventory file:**

    Modify the `hosts` file to include the target host information.

2. **Run the playbook:**
    ```sh
    ansible-playbook -i inventory playbook.yaml --ask-become-pass
    ```