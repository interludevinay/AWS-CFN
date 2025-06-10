# 🏗️ AWS CloudFormation Template for Baseline Infrastructure

## Overview
This project aims to develop a CloudFormation template that creates a baseline structure for a cloud infrastructure in AWS. The template will provision essential networking components, including a Virtual Private Cloud (VPC), subnets, routing tables, network access control lists (NACLs), and security groups.

![Image](https://github.com/user-attachments/assets/c100f654-228a-4270-9e3b-b9c0759536cf)

## Table of Contents
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Deployment Instructions](#deployment-instructions)
- [Template Structure](#template-structure)
- [Issues and Future Improvements](#issues-and-future-improvements)
- [Contributing](#contributing)
- [License](#license)

## Features
- **VPC Creation**: Provisions a custom VPC.
- **Subnets**: Creates multiple public and private subnets across different availability zones.
- **Routing Tables**: Configures route tables for connecting public and private subnets.
- **Internet Gateway**: Associates an Internet Gateway for external access.
- **NACLs**: Sets up Network Access Control Lists for enhanced security.
- **Security Groups**: Configures security groups to control inbound and outbound traffic.

## Prerequisites
- An AWS account with permissions to create the required resources.
- AWS CLI installed and configured.
- Basic understanding of AWS CloudFormation and networking concepts.

## Deployment Instructions
### Clone the Repository
```bash
git clone https://github.com/interludevinay/AWS-CFN.git
cd AWS-CFN/Base-line-structure
```

## Template Structure
```bash
---
AWSTemplateFormatVersion: version date

Description:
  String

Metadata:
  template metadata

Parameters:
  set of parameters

Mappings:
  set of mappings

Resources:
  set of resources
```

- **AWSTemplateFormatVersion:** Specifies the version of the AWS CloudFormation template format.

- **Description:** Briefly describes the purpose of the template.

- **Parameters:** Allows users to input values when launching the stack.

- **Mappings:** Provides a method for creating lookup tables for CIDR blocks and availability zones.

- **Resources:** Defines AWS resources to be created, including VPC, subnets, route tables, and network ACLs, along with their associations and configurations.

## Issues and Future Improvements

```
Currently, the YAML template might face issues with duplication.
A plan to improve and resolve these issues is in progress and will be addressed in future commits.
```

## Contributing
```
Fork the repository.
Create a new branch for your feature or bug fix.
Submit a pull request detailing your changes.
```
