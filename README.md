# AWS S3 Static Website Deployment using Terraform

## Overview

This project demonstrates the deployment of a **static website on Amazon S3** using **Terraform**.  
It follows modern AWS security best practices by disabling public ACLs and enabling public access through an **S3 bucket policy**.

The project highlights the use of **Infrastructure as Code (IaC)** to build a secure, cost-effective, and reproducible cloud setup.

---

## Architecture Summary

- **Amazon S3** – Static website hosting  
- **Terraform** – Infrastructure provisioning  
- **S3 Bucket Policy** – Secure public read access  
- **HTML / CSS / JavaScript** – Frontend content  

---

## Project Structure

```
S3_STATIC_WEB_TERRAFORM/
│
├── provider.tf                 # AWS provider configuration
├── variables.tf                # Input variables
├── main.tf                     # Infrastructure definition
├── output.tf                   # Output values
│
├── index.html                  # Static website homepage
├── error.html                  # Custom error page
└── README.md                   # Project documentation
```

---

## Key Features

- Infrastructure fully managed using Terraform
- Public access configured via bucket policy (no public ACLs)
- Custom error page support
- Compatible with AWS Free Tier
- Reproducible and maintainable design

---

## Prerequisites

- AWS account
- AWS CLI configured (`aws configure`)
- Terraform installed

---

## Deployment Instructions

### Initialize Terraform
```bash
terraform init
```

### Review the Execution Plan
```bash
terraform plan
```

### Apply the Configuration
```bash
terraform apply
```

After successful execution, Terraform outputs the **S3 static website endpoint URL**.

---

## Accessing the Website

- Open the website endpoint from Terraform output
- `index.html` is served as the landing page
- `error.html` is displayed for invalid paths

---

## Security Considerations

- Public ACLs are disabled
- Public access is granted using least-privilege bucket policy
- Only `s3:GetObject` permission is allowed
- No write or delete access is exposed

---

## Cost Management

This setup runs within **AWS Free Tier limits**:
- S3 storage up to 5 GB
- Minimal request usage
- No additional paid AWS services

To remove all resources and avoid charges:
```bash
terraform destroy
```

---

## Learning Outcomes

- Understanding S3 static website hosting
- Hands-on experience with Terraform
- Secure public access using bucket policies
- Managing cloud infrastructure using IaC
- Handling common AWS deployment scenarios

---

## Use Cases

- DevOps hands-on practice
- AWS and Terraform learning project
- Resume / portfolio demonstration
- Cloud fundamentals implementation

---

## Future Enhancements

- Add CloudFront for CDN and HTTPS
- Configure Route 53 for custom domain
- Integrate CI/CD pipeline for automated deployments

---

## Author

Developed as a professional DevOps learning project to demonstrate cloud automation and best practices.
