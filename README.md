# 🚀 Enterprise Active Directory Infrastructure Design & Implementation

## 📌 Overview

This project simulates a real-world enterprise IT environment using Microsoft Active Directory and Windows Server technologies. It demonstrates how to design, deploy, and secure a scalable infrastructure for a multi-branch organization.

The implementation follows industry best practices for identity management, access control, and system administration.

---

## 🏢 Business Scenario

A company named **TechCorp Solutions** operates a headquarters (HQ) and two branch offices. The organization requires:

* Centralized authentication system
* Secure access to company resources
* Controlled file sharing between departments
* Enforced security policies
* Scalable and fault-tolerant infrastructure

This project addresses all these requirements using Active Directory and supporting services.

---

## 🏗️ Architecture Summary

* **Domain:** techcorp.local

* **Forest Model:** Single Forest / Single Domain

* **Sites:** HQ, Branch1, Branch2

* **Domain Controllers:**

  * DC1 (Primary – HQ)
  * DC2 (Secondary – Branch1)

* **Core Services:**

  * Active Directory Domain Services (AD DS)
  * DNS
  * DHCP
  * File Server

* **Network Subnets:**

  * HQ: 192.168.1.0/24
  * Branch1: 192.168.2.0/24
  * Branch2: 192.168.3.0/24

* **Connectivity:** VPN tunnels between branches

---

## 🗂️ Active Directory Design

### Organizational Units (OUs)

* HQ (Users, Computers, Servers)
* Branch1 / Branch2
* Departments (HR, Finance, IT, Sales)
* Groups
* Service Accounts

### Group Strategy

Implemented **AGDLP model**:

* Accounts → Global Groups → Domain Local Groups → Permissions

---

## ⚙️ Features Implemented

### 🔐 Security

* Password complexity enforcement
* Account lockout policies
* Least privilege access model
* Audit logging (logon, object access, policy changes)

### 📜 Group Policy (GPO)

* Security baseline policies
* USB storage restriction
* Firewall enforcement
* Department-based restrictions
* Workstation hardening

### 📂 File Server

* Department-based shared folders
* NTFS + Share permissions
* Role-based access control

### 🌐 Network Services

* DNS for domain resolution
* DHCP for automatic IP assignment

### 💾 Backup Strategy

* System State backup (Active Directory)
* Scheduled backups for file server

---

## ⚡ Automation (PowerShell)

Scripts included:

* Create Organizational Units
* Bulk user creation (CSV-based)
* Backup automation

---

## 🛠️ Implementation Steps

1. Install Windows Server
2. Configure Domain Controller (DC1)
3. Add Secondary Domain Controller (DC2)
4. Configure DNS and DHCP
5. Create OUs, Users, and Groups
6. Apply Group Policies
7. Configure File Server and permissions
8. Implement backup strategy

Detailed steps available in `/docs/implementation-guide.md`

---

## 🧪 Troubleshooting

Common issues covered:

* GPO not applying → `gpupdate /force`
* Replication issues → `repadmin /replsummary`
* Login failures → DNS misconfiguration
* Permission issues → NTFS vs Share mismatch


---



## 🎯 Key Skills Demonstrated

* Active Directory Administration
* Group Policy Management
* Windows Server Infrastructure
* Network Services (DNS/DHCP)
* Security Hardening
* PowerShell Automation

---

