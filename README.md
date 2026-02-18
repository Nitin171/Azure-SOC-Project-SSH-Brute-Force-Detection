# Azure SOC Project – SSH Brute Force Detection

## 📌 Project Overview

This project demonstrates a real-world Security Operations Center (SOC) scenario by simulating SSH brute-force attacks on an Azure Linux Virtual Machine and detecting them using Microsoft Sentinel.

The goal was to design and implement an end-to-end cloud security monitoring pipeline capable of detecting unauthorized SSH login attempts, generating security incidents, and triggering automated alerts.

---

## 🎯 Objectives

- Deploy and secure an Azure Linux Virtual Machine
- Simulate SSH brute-force attacks
- Collect and analyze Linux authentication logs
- Detect suspicious login activity using KQL
- Automatically generate incidents in Microsoft Sentinel
- Trigger alert notifications using Azure Logic Apps

---

## 🏗 Architecture Overview

Azure Linux VM  
⬇  
Linux Authentication Logs (`/var/log/auth.log`)  
⬇  
Log Analytics Workspace  
⬇  
Microsoft Sentinel (SIEM)  
⬇  
KQL Detection Rule  
⬇  
Incident Creation  


---

## 🛠 Technologies Used

- Microsoft Azure  
- Microsoft Sentinel (SIEM)  
- Azure Log Analytics  
- Azure Linux Virtual Machine  
- Network Security Groups (NSG)  
- UFW Firewall  
- Kusto Query Language (KQL)  


## 🔐 Security Hardening Implemented

- Configured Network Security Group (NSG) rules  
- Restricted SSH access to controlled IP ranges  
- Enabled UFW firewall on Linux VM  
- Disabled password-based authentication  
- Implemented SSH key-based authentication  
- Monitored and logged unauthorized login attempts  

---

## 🚨 Attack Simulation

A brute-force SSH attack was simulated against the Azure Linux VM to generate multiple failed authentication attempts.

This allowed validation of:

- Log ingestion pipeline  
- Detection accuracy  
- Incident generation  
- Alert workflow automation  

