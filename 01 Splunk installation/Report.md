# Session 01 — Windows SOC Lab Setup

**Date:** 20 July 2026

---

# Objective

Build the Windows SOC Lab from scratch and prepare a Windows 11 endpoint for future security monitoring, log collection, and attack simulations.

---

# Overview

This session focused on creating the foundation of the Windows SOC Lab by deploying a dedicated Windows 11 virtual machine. The system was configured with the required hardware resources, prepared for future security tooling, and a clean baseline snapshot was created before installing any monitoring applications.

---

# Lab Environment

| Component | Configuration |
|------------|---------------|
| Operating System | Windows 11 |
| Virtualization | Oracle VirtualBox |
| Endpoint Name | SOC-WIN11-01 |
| Administrator Account | SOCAdmin |
| RAM | 6144 MB |
| CPU | 4 Cores |
| Disk | 80 GB |

---

# Tasks Completed

- Verified Oracle VirtualBox installation.
- Downloaded the Windows 11 ISO.
- Created the Windows 11 virtual machine.
- Allocated 6144 MB RAM, 4 CPU cores, and an 80 GB virtual disk.
- Installed Windows 11.
- Renamed the endpoint to **SOC-WIN11-01**.
- Created the **SOCAdmin** local administrator account.
- Installed VirtualBox Guest Additions.
- Created the initial snapshot named **Clean Windows 11**.

---

# Screenshots

## Windows 11 Virtual Machine Configuration

> **Screenshot Placeholder**

*Figure 1. Virtual machine configuration in Oracle VirtualBox.*

---

## Windows 11 Installation

> **Screenshot Placeholder**

*Figure 2. Windows 11 installed successfully.*

---

## Renaming the Endpoint

> **Screenshot Placeholder**

*Figure 3. Computer renamed to SOC-WIN11-01.*

---

## Local Administrator Account

> **Screenshot Placeholder**

*Figure 4. SOCAdmin local administrator account created.*

---

## VirtualBox Guest Additions

> **Screenshot Placeholder**

*Figure 5. VirtualBox Guest Additions installed successfully.*

---

## Initial Snapshot

> **Screenshot Placeholder**

*Figure 6. Initial "Clean Windows 11" snapshot created.*

---

# Why This Matters

A clean baseline is essential for every SOC lab. Establishing a known-good system before installing security tools helps distinguish normal system activity from malicious behavior during future investigations. Creating snapshots also allows the environment to be restored quickly before testing new attack scenarios.

---

# Skills Practiced

- Windows 11 Deployment
- Virtual Machine Management
- Oracle VirtualBox Configuration
- Windows Endpoint Preparation
- Lab Planning
- Baseline Creation

---

# Lessons Learned

- A well-organized lab makes future investigations easier to perform.
- Creating snapshots before major changes simplifies recovery.
- Consistent endpoint naming improves organization and investigation.
- Building a reliable environment is the first step toward effective SOC operations.

---

# Session Outcome

- Windows 11 virtual machine deployed successfully.
- SOC endpoint configured.
- Clean baseline established.
- Initial recovery snapshot created.

The environment is now ready for endpoint monitoring and security tooling.

---

# Next Session

Deploy Sysmon, apply a recommended configuration, and verify endpoint telemetry using Windows Event Viewer.
