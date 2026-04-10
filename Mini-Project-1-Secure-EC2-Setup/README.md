# 🔐 Mini Project 1: Secure EC2 Setup

## 📋 Project Overview
**Days Covered:** 1 – 9  
**Goal:** Launch an EC2 instance and secure it with SSH-only access, stop and termination protection, and an upgraded instance type.

---

## 🛠️ Skills Demonstrated
- Key Pair creation and management
- Security Group configuration (SSH-only access)
- EC2 instance launch and configuration
- Stop and Termination protection
- Instance type upgrade (t2.micro → t3.micro)

---

## 📌 Steps Completed

**Day 1 — Create Key Pair**
Created RSA key pair named `my-keypair` for secure SSH access to the EC2 instance.

**Day 2 — Create Security Group**
Created security group `SG-SSH-Only` allowing inbound SSH (port 22) from my IP only. All other traffic blocked.

**Day 3 — Create Subnet**
Created a subnet within the default VPC to define the network boundary for the instance.

**Day 6 — Launch EC2 Instance**
Launched EC2 instance `Secure-EC2-1` (t2.micro) using Amazon Linux 2023 AMI, attached `my-keypair` and `SG-SSH-Only`.

**Day 7 — Change Instance Type**
Stopped the instance and upgraded from t2.micro to t3.micro for improved performance and cost efficiency.

**Day 8 — Enable Stop Protection**
Configured stop protection to prevent accidental stopping of the instance.

**Day 9 — Enable Termination Protection**
Enabled termination protection to prevent accidental deletion of the instance.

---

## 📸 Screenshots

| Step | Screenshot |
|------|------------|
| Key Pair Created | ![Key Pair](./screenshots/01-Key-Pair-Created.png) |
| Security Group Created | ![Security Group](./screenshots/02-Security-Group-Created.png) |
| Instance Launched | ![Instance Launched](./screenshots/03-Instance-Launched.png) |
| Instance Running | ![Instance Running](./screenshots/04-Instance-Running.png) |
| Termination Protection Enabled | ![Protection](./screenshots/05-Termination-Protection-Enabled.png) |
| Stop Protection Test | ![Stop Test](./screenshots/06-Stop-Protection-Test.png) |
| Instance Type Changed | ![Type Changed](./screenshots/07-Instance-Type-Changed.png) |
| Instance Running as t3.micro | ![t3 Running](./screenshots/08-Instance-Running-t3micro.png) |
| Project Complete | ![Complete](./screenshots/09-Project-Complete.png) |

---

## 💡 Key Learnings
- EC2 instances have dynamic public IPs by default — they change on restart
- Security groups act as virtual firewalls — restricting to SSH-only reduces attack surface
- Stop and termination protection are critical safeguards in production environments
- Instance types can be changed without recreating the instance — requires a stop first

---

## ✅ Outcome
Successfully launched and secured an EC2 instance with SSH-only access, dual protection enabled, and upgraded to t3.micro.
