# Project 3: RDS Database Creation: Deploying a MySQL Database
<div align="center"><img width="70%" src="https://github.com/user-attachments/assets/d7596a89-8bea-4a71-8b0f-3b125b750034"></div>

Create a managed MySQL database using Amazon RDS and connect it to a simple application.

## **AWS Services Used**
- RDS (Relational Database Service)
- EC2


## **Step 1: Launch an RDS Instance**
1. Open the **RDS Console** in the AWS Management Console.
2. Click **Create Database**.
   - Choose **Standard Create** and select **MySQL** as the engine type.
   - Select the Free Tier template.
3. Configure settings:
   - Set a DB instance identifier (e.g., `my-mysql-db`).
   - Choose a master username and password.
   - Allocate storage (default is 20 GB).
4. Configure connectivity:
   - Select **Public Access** and choose a VPC.
   - Create a new security group to allow MySQL traffic (port 3306).
5. Enable backups and monitoring options (optional).
6. Click **Create Database**.

---

## **Step 2: Connect to the Database**
1. Note the endpoint URL of your RDS instance from the RDS Console.
2. Launch an EC2 instance and install the MySQL client:
   ```bash
   sudo yum update -y
   sudo yum install mysql -y
3. Connect to the database:
   ```bash
   mysql -h <endpoint-url> -u admin -p
4. Create a test database and table:
   ```sql
   CREATE DATABASE testdb;
   USE testdb;
   CREATE TABLE users (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(255));
   INSERT INTO users (name) VALUES ('John Doe');
   SELECT * FROM users;


## Conclusion
You’ve successfully created a managed MySQL database using Amazon RDS and connected it to a simple application. RDS simplifies database management, allowing you to focus on building your application
