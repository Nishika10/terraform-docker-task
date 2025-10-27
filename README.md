# Infrastructure as Code (IaC) with Terraform

This project demonstrates how to use Terraform to provision and manage a Docker container, showcasing the concept of Infrastructure as Code (IaC).
## Tech / Tools Used

- Terraform – Infrastructure automation

- Docker – Containerization platform

- Ubuntu (AWS EC2 Instance) – Execution environment

## Installation

Run the following commands to set up the environment:

### Install Docker
```bash
sudo apt update
sudo apt install -y docker.io
sudo systemctl start docker
sudo systemctl enable docker
```

### Install Terraform
```bash
wget https://releases.hashicorp.com/terraform/1.6.3/terraform_1.6.3_linux_amd64.zip
unzip terraform_1.6.3_linux_amd64.zip
sudo mv terraform /usr/local/bin/
terraform version
```
## Run Locally

Clone the repository and execute Terraform commands to create and manage the Docker container.

1. **Initialize Terraform**
```bash
terraform init
```
2. **View the execution plan**
```bash
terraform plan
```

3. **Apply configuration to create container**
```bash
terraform apply
```

4. **Check Terraform state**
```bash
terraform state list
```

5. **Destroy the infrastructure**
```bash
terraform destroy
```

## Usage / Examples

This Terraform configuration provisions a Docker container running Nginx.
After applying the configuration, the Nginx web server runs successfully on the container.


## Screenshots

### 1. Terraform Init  
Shows successful initialization of the Terraform working directory and Docker provider.  
![Terraform Init Screenshot](screenshots/terraform-init.png)

### 2. Terraform Apply  
Shows successful creation of the Docker container using Terraform.  
![Terraform Apply Screenshot](screenshots/terraform-apply.png)

### 3. Terraform State List  
Displays the list of managed resources after successful deployment.  
![Terraform State List Screenshot](screenshots/terraform-state-list.png)

### 4. Running Nginx Locally  
Demonstrates that the Nginx container is running successfully and accessible on the local port (http://localhost:8080).  
![Nginx Localhost Screenshot](screenshots/nginx-localhost.png)

### 5. Terraform Destroy  
Shows successful destruction of the Docker container and image after cleanup.  
![Terraform Destroy Screenshot](screenshots/terraform-destroy.png)






