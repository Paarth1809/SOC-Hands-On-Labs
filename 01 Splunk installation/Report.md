# Session 01 — Windows SOC Lab Setup

**Date:** 20 July 2026

---

## Objective

Build the foundation of the Windows SOC Lab by creating and configuring a dedicated Windows 11 virtual machine that will be used for future security monitoring, log collection, and attack simulations.

---

## Overview

This session focused on setting up a clean Windows 11 endpoint inside VirtualBox. The virtual machine was configured with appropriate hardware resources, renamed for easier identification, and prepared with an administrator account. A clean snapshot was also created to provide a reliable restore point before installing security tools such as Sysmon and Splunk.

---

## Lab Environment

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

## Tasks Completed

- Verified VirtualBox installation.
- Downloaded the Windows 11 ISO.
- Created a new Windows 11 virtual machine.
- Allocated 6144 MB RAM, 4 CPU cores, and an 80 GB virtual disk.
- Installed Windows 11.
- Renamed the system to **SOC-WIN11-01**.
- Created the **SOCAdmin** local administrator account.
- Installed VirtualBox Guest Additions.
- Created the initial snapshot named **Clean Windows 11**.

---

## Screenshots

### Windows 11 Virtual Machine Configuration

![Virtual Machine Configuration](screenshots/01-vm-configuration.png)

*Figure 1. Virtual machine hardware configuration in Oracle VirtualBox.*

---

### Windows 11 Installation Completed

![Windows Installation](screenshots/02-windows-installation.png)

*Figure 2. Windows 11 installed successfully.*

---

### Computer Name Changed

![Computer Name](screenshots/03-computer-name.png)

*Figure 3. Endpoint renamed to SOC-WIN11-01.*

---

### Local Administrator Account

![Administrator Account](screenshots/04-socadmin.png)

*Figure 4. SOCAdmin local administrator account created.*

---

### VirtualBox Guest Additions

![Guest Additions](screenshots/05-guest-additions.png)

*Figure 5. VirtualBox Guest Additions installed successfully.*

---

### Initial Snapshot

![Snapshot](screenshots/06-clean-snapshot.png)

*Figure 6. Initial "Clean Windows 11" snapshot created.*

---

## Why This Matters

A clean and well-documented baseline is essential for any SOC lab. It provides a known-good system state before security tools are installed or attack simulations are performed. Creating an initial snapshot also makes it easy to restore the environment if a future experiment causes unexpected issues.

---

## Skills Practiced

- Virtual machine deployment
- Windows 11 installation
- VirtualBox configuration
- Windows endpoint preparation
- Lab environment setup
- Baseline creation

---

## Lessons Learned

- A well-prepared environment makes future labs easier to manage.
- Creating snapshots before major changes helps prevent data loss.
- Consistent endpoint naming improves organization and investigation.
- Establishing a clean baseline is an important first step before collecting security telemetry.

---

## Session Outcome

✅ Windows 11 virtual machine deployed successfully.

✅ Windows endpoint configured.

✅ Initial administrator account created.

✅ Clean baseline snapshot created.

The environment is now ready for the installation of endpoint monitoring and logging tools.

---

## Next Session

Deploy Sysmon using the SwiftOnSecurity configuration, verify Windows Event Viewer logs, and prepare the endpoint for SIEM log collection.
