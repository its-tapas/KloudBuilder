# Project 1: AWS Account Setup & IAM Basics
<div align="center">![AWS](https://github.com/user-attachments/assets/d334606b-66d0-4fe3-9584-6533908cb289)</div>


## **Description**
Learn how to create an AWS account, set up billing alerts, and configure IAM users and roles. This guide will walk you through creating an IAM user with billing access.

## **AWS Services Used**
- AWS Management Console
- IAM (Identity and Access Management)

---

## **Step-by-Step Guide**

### **Step 1: Create an AWS Account**
1. Go to the [AWS Sign-Up Page](https://aws.amazon.com/).
2. Enter your email address and click **Create a new AWS account**.
3. Fill in your personal information, including your name, password, and contact details.
4. Complete the payment method verification by entering your credit card details.
5. Verify your phone number via SMS or voice call.
6. Choose a support plan (Basic is free).

---

### **Step 2: Set Up Billing Alerts**
<div align="center">![Billing and budget](https://github.com/user-attachments/assets/b0023fcf-4603-4b67-b77e-82e9134b0430)</div>

1. Log in to the AWS Management Console.
2. Navigate to **Billing and Cost Management** from the top-right dropdown menu under your account name.
3. In the left-hand menu, click **Budgets**.
4. Click **Create Budget**.
   - Select **Cost Budget** and click **Set Your Budget**.
   - Set a budget limit (e.g., $10) and configure notifications for when your spending exceeds the threshold.
5. Save your budget configuration.

---
### **Step 3: Configure IAM Users and Roles**
<div align="center">![IAM-Identities-and-permission](https://github.com/user-attachments/assets/a84357f0-86e5-417d-9cef-a9b79bd5c64b)</div>
1. Open the **IAM Console** from the AWS Management Console.
2. In the left-hand menu, click **Users** and then **Add User**.
   - Enter a username (e.g., `billing-admin`).
   - Select **Programmatic access** and/or **AWS Management Console access**.
   - Click **Next: Permissions**.
3. Attach permissions:
   - Under **Set Permissions**, choose **Attach existing policies directly**.
   - Search for and select the policy `Billing`.
   - Click **Next: Tags** (optional).
4. Add tags if needed (e.g., `Environment: Production`), then click **Next: Review**.
5. Review the user details and click **Create User**.
6. Download the `.csv` file containing the access key and secret key for programmatic access.

---

### **Step 4: Test IAM User Access**
1. Log out of your root account.
2. Use the credentials provided for the IAM user to log in to the AWS Management Console.
3. Verify that the user can access billing information.

---

## **Conclusion**
You’ve successfully created an AWS account, set up billing alerts, and configured an IAM user with billing access. These foundational steps are crucial for managing your AWS resources securely and efficiently.
