# Self-Healing-AWS-Infrastructure
Automated self-healing EC2 architecture using AWS Lambda, CloudWatch, and SNS
# 🧠 Self-Healing AWS Infrastructure

This project demonstrates a **self-healing EC2 environment** on AWS that automatically detects failed or stopped instances and recovers them using **Lambda, CloudWatch, and SNS**.

---

## 🧩 Architecture
![Architecture Diagram](docs/architecture-diagram.png)

**Flow:**
1. CloudWatch detects EC2 failure.
2. EventBridge triggers a Lambda function.
3. Lambda restarts the instance.
4. SNS notifies admin via email.

---

## ⚙️ AWS Components
- EC2 (Application instance)
- CloudWatch (Monitoring & Alarms)
- Lambda (Recovery automation)
- SNS (Email notifications)
- IAM (Access control)

---

## 🚀 Steps to Deploy
1. Launch an EC2 instance  
2. Create an SNS topic and confirm subscription  
3. Create IAM role for Lambda  
4. Deploy the Lambda function (`lambda/ec2_self_healer.py`)  
5. Create CloudWatch Event Rule for EC2 state change  
6. Test by stopping the EC2 instance  

---

## 📧 Notifications
SNS will send an alert whenever the EC2 instance is stopped or recovered automatically.

---

## 🧰 Tech Stack
- AWS Lambda (Python 3.9)
- Boto3 SDK
- CloudWatch Events
- SNS Notifications
- Terraform (optional)

---

## 🧾 License
MIT License © 2025 Rajesh Kumar
