# AWS CloudFormation Template: EC2, S3, VPC, and Subnet

## 📌 Description

This CloudFormation template provisions core AWS infrastructure components using a declarative approach. It includes:

- A **VPC** with DNS support
- A **Subnet** within the VPC
- An **S3 Bucket**
- An **EC2 Instance** deployed in the subnet

## 🧩 Components Created

| Resource Type     | Resource Logical ID | Notes                                      |
|-------------------|---------------------|--------------------------------------------|
| VPC               | `CFNVPCR`           | With DNS Hostnames and Support enabled     |
| Subnet            | `CFNSubnetR`        | Custom CIDR block, linked to the VPC       |
| S3 Bucket         | `CFNS3R`            | Bucket name passed as a parameter          |
| EC2 Instance      | `CFNEC2R`           | AMI ID passed as a parameter               |

## 🛠️ Parameters

- `S3bucketnameP`: Name of the S3 bucket to create.
- `EC2imageIDP`: AMI ID for the EC2 instance (dropdown selection).
- `VPCIDP`: CIDR block for the VPC (dropdown selection).
- `VPCSubnetR`: CIDR block for the Subnet.

## 🧱 Architecture

![Image](https://github.com/user-attachments/assets/6fb858ad-c279-4cff-8ed2-cc13804b1bca)

## 🚀 Deployment

To deploy this template via AWS CLI:

```bash
aws cloudformation create-stack \
  --stack-name MyInfraStack \
  --template-body file://template.yaml \
  --parameters \
    ParameterKey=S3bucketnameP,ParameterValue=my-unique-bucket-name \
    ParameterKey=EC2imageIDP,ParameterValue=ami-05fa00d4c63e32376 \
    ParameterKey=VPCIDP,ParameterValue=10.0.0.0/16 \
    ParameterKey=VPCSubnetR,ParameterValue=10.0.1.0/24 \
  --capabilities CAPABILITY_NAMED_IAM
OR
```
use AWS comsole directly
```
## ⚠️ Ensure the AMI ID is valid in your region and the bucket name is globally unique.
