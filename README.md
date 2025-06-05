# 🏗️ AWS CloudFormation Projects — Complete IaC Portfolio with AWS CLI

Welcome to the ultimate AWS CloudFormation repository! This repo is a **centralized collection of real-world Infrastructure as Code (IaC) projects** using **AWS CloudFormation** and deployed via the **AWS CLI**. It’s designed for professionals, learners, and teams aiming to automate cloud infrastructure using modern DevOps practices.

---

## 🌐 Repository Purpose

This repository serves as a **one-stop portfolio** for AWS projects entirely managed through **CloudFormation templates**. Every project is written in YAML and follows IaC principles for scalability, repeatability, and automation.

---

## 🔧 Technologies & Tools

- **AWS CloudFormation** – Define your infrastructure in YAML
- **AWS CLI** – For deploying and managing stacks
- **IaC (Infrastructure as Code)** – Automate infrastructure setup
- **Version Control** – Every project is Git-tracked and modular

---

## 📚 What This Repo Will Contain

This repository is being continuously updated to include templates for:

- ✅ Basic infrastructure setups (EC2, S3, VPC, Subnets)
- 🚀 Auto Scaling, Load Balancers (ALB/NLB)
- 🔐 IAM roles and policies
- 💾 RDS & DynamoDB databases
- ☁️ Serverless apps with Lambda, API Gateway
- 📡 Networking (VPC peering, NAT Gateway, Route Tables)
- 📈 Monitoring with CloudWatch
- 📥 SQS, SNS, EventBridge, Step Functions
- 🔄 CI/CD Stack integrations (CodePipeline, CodeBuild)

Each folder contains:
- `template.yaml` — The CloudFormation template
- `README.md` (optional) — Description of the stack and deployment steps

---

## 🚀 How to Deploy a Stack

### 1. Create a Stack

```bash
aws cloudformation create-stack \
  --stack-name <stack-name> \
  --template-body file://template.yaml \
  --parameters ParameterKey=ParamName,ParameterValue=ParamValue
```

### 2. Update the stack

```bash
aws cloudformation update-stack \
  --stack-name <stack-name> \
  --template-body file://template.yaml
```

### 3. Delete the stack

```bash
aws cloudformation delete-stack \
  --stack-name <stack-name>
```
