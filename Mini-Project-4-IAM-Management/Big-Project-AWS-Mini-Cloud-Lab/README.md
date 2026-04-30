# ☁️ AWS Mini Cloud Lab: Full Cloud Architecture Project

## 📌 Project Overview

This project combines all previously learned AWS skills into a single, working cloud environment. Rather than isolated exercises, this lab connects multiple AWS services into a realistic cloud architecture demonstrating how they work together in production.

---

## 🎯 Objectives

- Design a full cloud architecture diagram before building
- Configure secure network access using Security Groups
- Launch and harden an EC2 instance with stop and termination protection
- Assign a stable public IP using Elastic IP
- Attach persistent storage with an EBS volume
- Back up data using EBS snapshots and AMI
- Configure IAM users and roles for secure access control

---

## 🛠️ AWS Services Used

| Service | Purpose |
|---|---|
| Amazon EC2 | Main compute instance (mini-cloud-lab-instance) |
| Security Groups | SSH-only access (Port 22) |
| Elastic IP | Stable public IP address (54.84.226.115) |
| Amazon EBS | Persistent block storage (gp3, 10 GiB) |
| EBS Snapshots | Point-in-time data backup |
| Amazon AMI | Full instance image for recovery |
| IAM Users | Secure user access (aws-dev) |
| IAM Roles | EC2 service role (EC2-Lab-Role) |

---

## 🏗️ Architecture Diagram

![Architecture Diagram](screenshots/01-architecture-diagram.jpg)

---

## 🪜 Steps Taken

### 1. IAM User Created
Created IAM user with limited permissions. IAM Dashboard shows 1 user group, 1 user, 4 roles, and 1 policy configured.

![IAM User Created](screenshots/02-iam-user-created.jpg)

---

### 2. IAM Role Created
Created `EC2-Lab-Role` trusted by the EC2 service, allowing the instance to securely interact with AWS resources.

![IAM Role Created](screenshots/03-iam-role-created.jpg)

---

### 3. Security Group Configured
Created security group `mini-cloud-lab-sg` with SSH access only (TCP Port 22), enforcing least-privilege network access.

![Security Group Created](screenshots/04-security-group-created.jpg)

---

### 4. EC2 Instance Launched
Successfully launched `mini-cloud-lab-instance` (t2.micro) in us-east-1c with EC2-Lab-Role attached.

![EC2 Instance Launched](screenshots/05-ec2-instance-launched.jpg)

---

### 5. Stop Protection Enabled
Enabled stop protection to prevent the instance from being accidentally stopped.

![Stop Protection Enabled](screenshots/06-stop-protection-enabled.jpg)

---

### 6. Termination Protection Enabled
Enabled termination protection to prevent accidental deletion of the instance.

![Termination Protection Enabled](screenshots/07-termination-protection-enabled.jpg)

---

### 7. Elastic IP Allocated
Allocated Elastic IP `54.84.226.115` for a stable, persistent public address.

![Elastic IP Allocated](screenshots/08-elastic-ip-allocated.jpg)

---

### 8. EBS Volume Attached
Successfully attached gp3 volume (10 GiB) to the instance for persistent storage.

![EBS Volume Attached](screenshots/09-ebs-volume-attached.jpg)

---

### 9. Snapshot Created
Created snapshot `snap-04fce12d8ab819cde` from the attached EBS volume as a point-in-time backup.

![Snapshot Created](screenshots/10-snapshot-created.jpg)

---

### 10. AMI Created
Initiated creation of AMI `ami-02032044482deed9f6` for full instance recovery capability.

![AMI Created](screenshots/11-ami-created.jpg)

---

### 11. IAM Role Attached to EC2
Successfully attached `EC2-Lab-Role` to `mini-cloud-lab-instance`, completing the secure access configuration.

![IAM Role Attached](screenshots/12-iam-role-attached-to-ec2.jpg)

---

## 💡 Key Learnings

- **Architecture-first thinking** — designing before building leads to cleaner, more intentional infrastructure
- **Defense in depth** — combining Security Groups, IAM roles, and instance protection creates multiple security layers
- **AWS services are interconnected** — EC2, EBS, IAM, and networking work together, not in isolation
- **Backup strategy matters** — snapshots protect data while AMIs protect the full system configuration
- **Elastic IP ensures reliability** — a stable IP prevents disruption if an instance is restarted

---

## ✅ Status: Complete

---

*Part of my [AWS Cloud Projects Portfolio](https://github.com/BlessingRakoma/AWS-Cloud-Projects)*
