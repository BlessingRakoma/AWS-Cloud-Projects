# 🔐 Mini Project 4: IAM User & Role Management

## 📌 Project Overview

This project focuses on managing secure access using AWS Identity and Access Management (IAM). The goal was to implement least-privilege access by creating users, groups, policies, and roles.

---

## 🎯 Objectives

- Create an IAM user with appropriate credentials
- Create a user group with defined permissions
- Design and attach a custom EC2 read-only policy
- Assign the user to the group
- Create an IAM role for EC2 with appropriate permissions

---

## 🛠️ AWS Services Used

| Service | Purpose |
|---|---|
| IAM Users | Created individual user `aws-dev` |
| IAM User Groups | Created `ReadOnly-EC2` group |
| IAM Policies | Created custom `EC2-ReadOnly-Policy` |
| IAM Roles | Created `EC2-ReadOnly-Role` for EC2 service |

---

## 🪜 Steps Taken

### 1. IAM User Created
Created IAM user `aws-dev` and assigned to a group for managed permissions.

![IAM User Created](screenshots/01-iam-user-created.jpg)

---

### 2. User Group Created
Created user group `ReadOnly-EC2` with 1 user and defined permissions policy.

![User Group Created](screenshots/02-user-group-created.jpg)

---

### 3. Custom Policy Created
Designed and attached a customer managed policy `EC2-ReadOnly-Policy` used as a permissions policy in 2 places.

![Custom Policy Created](screenshots/03-custom-policy-created.jpg)

---

### 4. IAM Role Created
Created IAM role `EC2-ReadOnly-Role` trusted by the EC2 service for secure access.

![IAM Role Created](screenshots/04-iam-role-created.jpg)

---

## 💡 Key Learnings

- **IAM is the foundation of cloud security** — controlling who can access what is critical in any cloud environment
- **Least privilege principle** means granting only the minimum permissions needed
- **User groups** make permission management scalable — change the group policy and all users inherit it
- **IAM roles** allow AWS services like EC2 to securely interact with other AWS resources without storing credentials

---

## ✅ Status: Complete

---

*Part of my [AWS Cloud Projects Portfolio](https://github.com/BlessingRakoma/AWS-Cloud-Projects)*
