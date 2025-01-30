
# AWS CLI Setup and Basic Commands
<div align="center"><img width="70%" src="https://github.com/user-attachments/assets/f8f2fd8b-c85b-43a5-bbcb-8aac50bb1c7c"></div>

Install the AWS CLI on Windows and learn basic commands for interacting with services like IAM, S3, and EC2.

## **AWS Services Used**
- IAM
- S3
- EC2

---

# **Step-by-Step Guide**

## **Step 1: Install AWS CLI**
1. Download the AWS CLI installer for Windows from the [official AWS CLI page](https://aws.amazon.com/cli/).
2. Run the installer and follow the prompts to complete installation.
3. Open Command Prompt and verify the installation:
   ```bash
   aws --version

## **Step 2: Configure AWS CLI**
1. Run the following command to configure the CLI:
   ```bash
   aws configure
2. Enter your AWS Access Key ID, Secret Access Key, region (e.g., ap-south-1), and output format (e.g., json).

## **Step 3: Basic AWS CLI Commands**

### IAM Commands
  - List IAM users;
     ```bash
     
     aws iam list-users
    
  - Create a new IAM user:
  
     ```bash
     
    aws iam create-user --user-name my-new-user

### S3 Commands
  - Create a bucket
     ```bash
     
    aws s3 mb s3://my-new-bucket
     
  - Upload a file
     ```bash
     
    aws s3 cp example.txt s3://my-new-bucket/

### EC2 Commands
  - List EC2 instances
     ```bash
     
    aws ec2 describe-instances
    
  - Start an EC2 instance
     ```bash
     
    aws ec2 start-instances --instance-ids <instance-id>

## Conclusion
You’ve successfully installed and configured the AWS CLI on Windows and learned basic commands for interacting with IAM, S3, and EC2. The AWS CLI is a powerful tool for automating tasks and managing your AWS resources programmatically.
