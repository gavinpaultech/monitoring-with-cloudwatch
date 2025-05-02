# ☁️ Simple EC2 Monitoring with CloudWatch ⌚

This project walks through setting up a basic Amazon EC2 instance and monitoring its CPU utilization using **Amazon CloudWatch**. You’ll create an alarm that triggers when CPU usage exceeds 15%, generate stress on the instance, and observe CloudWatch in action.

---

## 📋 Prerequisites

- AWS account
- IAM user with EC2 and CloudWatch permissions
- AWS CLI configured (optional)
- Basic knowledge of EC2 and Linux commands

---

## 🚀 Steps Overview

1. Launch a t2.micro EC2 instance in the default VPC with a public IP.
2. Connect to the instance and install required packages.
3. Create a CloudWatch alarm to monitor CPU usage.
4. Generate CPU load using `stress`.
5. Observe the CloudWatch alarm trigger and reset.
6. Clean up AWS resources.

---

## 🖥️ EC2 Setup

- **Instance Type**: `t2.micro`
- **VPC**: Default
- **Public IP**: Enabled
- **Monitoring**: Detailed monitoring (optional, small fee may apply)

---

## 🔧 Instance Configuration

SSH into your EC2 instance, then run:

```bash
sudo yum install stress -y
stress -c 1 -t 3600
```

