# 🌐 Mini Project 2: Elastic IP & Network Interfaces

## 📋 Project Overview
**Goal:** Make an EC2 instance reachable via a static public IP and configure a secondary network interface.

---

## 🛠️ Skills Demonstrated
- Elastic IP allocation and association
- Elastic Network Interface (ENI) creation and attachment
- EC2 networking configuration
- Static vs dynamic public IP management

---

## 📌 Steps Completed

**Allocate & Associate Elastic IP**
Allocated a static Elastic IP address (`100.49.73.177`) from AWS's public IP pool and associated it with EC2 instance `Secure-EC2-1`.

Why this matters: By default, EC2 public IPs change every time an instance is stopped and restarted. An Elastic IP ensures a consistent, static public address — critical for DNS records, application endpoints, and reliable server access.

**Create & Attach Secondary ENI**
Created a secondary Elastic Network Interface and attached it to the same EC2 instance as a secondary interface. Both ENIs are active and in-use, each with their own private IP address.

Why this matters: ENIs allow an instance to have multiple network interfaces — enabling network segmentation, dual-homed instances, and failover scenarios where a secondary interface can be moved between instances without changing the IP.

---

## 📸 Screenshots

| Step | Screenshot |
|------|------------|
| EC2 Instance with Elastic IP | ![EC2 Elastic IP](./screenshots/01-EC2-Instance-With-Elastic-IP.png) |
| EC2 Instance Details | ![EC2 Details](./screenshots/02-EC2-Instance-Details.png) |
| Elastic IP Detail Panel | ![Elastic IP Detail](./screenshots/03-Elastic-IP-Detail-Panel.png) |
| Both ENIs Attached | ![ENIs](./screenshots/04-Network-Interfaces-Both-ENIs.png) |

---

## 💡 Key Learnings
- Elastic IPs are static — they persist through instance stop/start cycles
- Without an Elastic IP, applications pointing to your instance break every time it restarts
- A single EC2 instance can have multiple ENIs — each with its own private IP
- ENIs are useful for network isolation, failover, and multi-homed architectures

---

## ✅ Outcome
Successfully assigned a static Elastic IP to EC2 instance `Secure-EC2-1` and attached a secondary ENI — giving the instance a stable public address and dual network interface configuration.
