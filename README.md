# 🛡️ Azure SOC Project – SSH Brute Force Detection

## 📌 Project Overview

This project demonstrates a real-world Security Operations Center (SOC) workflow in Microsoft Azure by detecting and investigating SSH brute-force attacks on a Linux virtual machine.

The lab simulates attacker behavior, collects authentication logs, builds detection rules using Microsoft Sentinel (SIEM), and investigates generated security incidents — replicating enterprise-level cloud threat detection and response.

---

## 🎯 Objectives

- Deploy and secure a Linux VM in Azure
- Simulate SSH brute-force attacks
- Collect authentication logs centrally
- Build detection rules using KQL
- Generate and investigate security incidents
- Validate end-to-end detection workflow

---

## 🏗️ Architecture

Internet (Attacker)
│
▼
Azure NSG (Network-level filtering)
│
▼
Linux VM (Inside VNet & Subnet)
│
├── UFW Firewall (OS-level protection)
├── SSH Hardening (Secure access control)
└── Fail2Ban (Automatic IP blocking)
│
▼
Azure Monitor Agent
│
▼
Log Analytics Workspace
│
▼
Microsoft Sentinel (SIEM)
│
▼
Incident Detection & Investigation

---

## ⚙️ Environment Setup

- Microsoft Azure Student Subscription
- Azure Linux Virtual Machine
- Virtual Network (VNet) & Subnet
- Network Security Group (NSG)
- Azure Monitor Agent
- Log Analytics Workspace
- Microsoft Sentinel

---

## 🔐 Security Hardening Implemented

### 🔹 Network-Level Protection
- Configured NSG rules to restrict inbound traffic
- Allowed only required ports (SSH – Port 22)

### 🔹 Host-Level Protection
- Enabled UFW firewall
- Disabled password-based SSH authentication
- Disabled root login
- Enforced key-based authentication

### 🔹 Intrusion Prevention
- Configured Fail2Ban to monitor authentication logs
- Automatically blocked IP addresses performing repeated failed login attempts

---

## 🧪 Attack Simulation

To validate detection capabilities, SSH brute-force attempts were simulated:

```bash
ssh fakeuser@<VM_Public_IP>

