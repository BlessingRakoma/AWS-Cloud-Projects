# 🗄️ Mini Project 3: EC2 Backup & Recovery

## 📌 Project Overview

This project focuses on understanding how cloud backups and recovery work in real-world AWS environments. The goal was to ensure an EC2 instance and its data can be safely backed up, restored, and recovered in the event of failure.

---

## 🎯 Objectives

- Create and attach an EBS volume to an EC2 instance
- Create EBS snapshots for data backup
- Create an Amazon Machine Image (AMI) for full instance backup
- Practice safe instance termination and verify recovery options
- Understand AWS disaster recovery concepts

---

## 🛠️ AWS Services Used

| Service | Purpose |
|---|---|
| Amazon EC2 | Host instance (Secure-EC2-1) |
| Amazon EBS | Persistent block storage (gp3, 8 GiB) |
| EBS Snapshots | Point-in-time data backup |
| Amazon AMI | Full instance image for recovery |

---

## 🪜 Steps Taken

### 1. EC2 Instance Running
Confirmed the EC2 instance `Secure-EC2-1` was running with termination protection enabled, then safely removed protection before cleanup.

![EC2 Instance Running](screenshots/01-ec2-instance-running.png)

---

### 2. EBS Volume Created
Created a gp3 EBS volume (8 GiB) in us-east-1c. Volume status showed as **Available**, ready for attachment.

![EBS Volume Created](screenshots/02-ebs-volume-created.png)

---

### 3. EBS Volume Attached
Successfully attached volume `vol-085c21e5f6b1427ae` to instance `i-0029fa48fd63733c8`. Volume state changed to **In-use**.

![EBS Volume Attached](screenshots/03-ebs-volume-attached.png)

---

### 4. Snapshot Created
Created snapshot `snap-0a73d037ec5d6b3ef` from the attached EBS volume as a point-in-time backup.

![Snapshot Created](screenshots/04-snapshot-created.png)

---

### 5. AMI Created
Created Amazon Machine Image `MiniProject3-AMI` (ami-0d7a926aded836955) for full instance recovery capability.

![AMI Created](screenshots/05-ami-created.png)

---

### 6. Instance Terminated
Successfully terminated the EC2 instance after completing backup verification, demonstrating safe shutdown procedures.

![Instance Terminated](screenshots/06-instance-terminated.png)

---

## 💡 Key Learnings

- **EBS Snapshots** provide point-in-time backups of individual volumes and can be used to restore or create new volumes
- **AMIs** capture the full instance configuration, enabling complete instance recovery with one click
- **Termination protection** is a critical safeguard that must be deliberately disabled before an instance can be deleted
- Understanding the difference between volume-level and instance-level backup is essential for real-world disaster recovery planning

---

## ✅ Status: Complete

---

*Part of my [AWS Cloud Projects Portfolio](https://github.com/BlessingRakoma/AWS-Cloud-Projects)*
