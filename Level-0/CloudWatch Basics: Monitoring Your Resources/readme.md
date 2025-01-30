# CloudWatch Basics: Monitoring Your Resources

 <div align="center"><img width="70%" src="https://github.com/user-attachments/assets/ffafb8da-e88e-45f0-8ebb-434b42be0baf"></div>
Set up basic monitoring for your AWS resources using CloudWatch metrics and alarms. This guide will show you how to monitor an EC2 instance.

## **AWS Services Used**
- CloudWatch
- EC2

---

## **Step-by-Step Guide**

### **Step 1: Launch an EC2 Instance**
1. Open the **EC2 Console** in the AWS Management Console.
2. Click **Launch Instance**.
   - Choose an Amazon Machine Image (AMI), such as Amazon Linux 2.
   - Select an instance type (e.g., t2.micro).
   - Configure instance details and storage settings.
3. Add tags (optional) and configure security groups to allow SSH access.
4. Launch the instance and download the key pair.

---

### **Step 2: Enable CloudWatch Metrics**
1. In the EC2 Console, select your instance and go to the **Monitoring** tab.
2. Click **View All Metrics** to open the CloudWatch Console.
3. Explore default metrics like CPU utilization, network traffic, and disk I/O.

---

 <div align="center"><img width="70%" size="50%" src="https://github.com/user-attachments/assets/64a57855-0b97-412c-ba5f-003baf3e9257"></div>

---

### **Step 3: Create a CloudWatch Alarm**
1. In the **CloudWatch Console**, click **Alarms** in the left-hand menu.
2. Click **Create Alarm**.
   - Select the metric **CPUUtilization** for your EC2 instance.
   - Set a threshold (e.g., alarm when CPU usage exceeds 80% for 5 minutes).
3. Configure actions:
   - Choose **Send Notification** and create an SNS topic to send email alerts.
   - Add recipients' email addresses.
4. Name your alarm and click **Create Alarm**.

---

### **Step 4: Test the Alarm**
1. SSH into your EC2 instance and run a command to simulate high CPU usage:
   ```bash
   yes > /dev/null &
2. Monitor the alarm status in the CloudWatch Console.
3. Once the alarm triggers, stop the process
   ```bash
   killall yes

---

### **Conclusion**
You’ve successfully set up CloudWatch monitoring and alarms for your EC2 instance. CloudWatch is a powerful tool for tracking resource performance and ensuring your applications run smoothly.
