# Terraform Learning Journey

## Day 1 - Terraform Basics

### Topics Covered

- Installed Terraform on Windows
- Added Terraform to PATH
- Verified installation using:

  ```bash
  terraform version
  ```

- Upgraded Terraform from v1.15.1 to v1.15.5
- Installed and configured Git
- Created a GitHub repository

### Terraform Concepts Learned

#### What is Terraform?

Terraform is an Infrastructure as Code (IaC) tool used to create, manage, and destroy infrastructure using code.

#### What is IaC?

Infrastructure as Code (IaC) is the practice of managing infrastructure through code instead of manual configuration.

#### Terraform Workflow

- `terraform init` → Setup project and download providers
- `terraform plan` → Preview changes
- `terraform apply` → Create or update infrastructure
- `terraform destroy` → Delete infrastructure

### First Terraform Project

Created a local file using Terraform.

```hcl
terraform {
  required_providers {
    local = {
      source = "hashicorp/local"
    }
  }
}

resource "local_file" "hello" {
  filename = "hello.txt"
  content  = "Hello Terraform!"
}
```

### Concepts Learned from the Project

#### Provider

```hcl
local
```

The provider tells Terraform what platform or service it should interact with.

#### Resource

```hcl
resource "local_file" "hello"
```

A resource is an object Terraform creates and manages.

### Git Commands Learned

```bash
git init
git status
git add .
git commit -m "message"
git remote add origin <repo-url>
git push -u origin main
```

### Day 1 Outcome

- Learned Terraform fundamentals
- Created first Terraform resource
- Understood provider and resource concepts
- Learned basic Git workflow
- Published project to GitHub

---

Next Topic: Variables and Outputs
