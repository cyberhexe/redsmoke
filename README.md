# General Information

A command-and-control (C2) server manageable via Terraform.

Includes:
- A free-tier Kali image
- A free-tier instance type (t2.micro)
- Pre-configured firewall rules (security groups) for communicating with your instance via SSH
- SSH keys being auto-generated and preconfigured per instance creation


# Installation

### Installing AWS CLI
```bash
apt install awscli
aws configure
```

### Installing Terraform (Ubuntu)
```bash
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
sudo apt-get update && sudo apt-get install terraform
```

### Cloning redform
```bash
git clone https://github.com/cyberhexe/redform
```

# Usage

### Creating the infrastructure 
```bash
cd redform
cd c2
terraform init
terraform apply -auto-approve
```

### Destroying the infrastructure
```bash
cd c2
terraform destroy -auto-approve
```
