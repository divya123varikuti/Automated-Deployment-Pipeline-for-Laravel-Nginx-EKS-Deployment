# Automated-Deployment-Pipeline-for-Laravel-Nginx-EKS-Deployment

## Setup Instructions

### 1. Local Setup
- Clone the repository.
- Build the Docker container:
  ```bash
  docker build -t laravel-nginx .
  ```
- Run the container:
  ```bash
  docker run -p 8080:80 laravel-nginx
  ```

### 2. CI/CD Pipeline
- Configure Jenkins or GitLab with the provided pipeline configuration.
- Trigger the pipeline by pushing to the repository.

### 3. Infrastructure Provisioning
- Navigate to the `terraform/` directory:
  ```bash
  terraform init
  terraform apply
  ```

### 4. Kubernetes Deployment
- Use Ansible to deploy:
  ```bash
  ansible-playbook ansible/playbook.yml
  ```

### 5. Verification
- Access the application via the LoadBalancer URL provided by Kubernetes.
