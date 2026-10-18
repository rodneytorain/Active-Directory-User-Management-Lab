# Active-Directory-User-Management-Lab

This project documents the setup of a Windows Server Active Directory environment used to practice domain administration, organizational unit design, user provisioning, DNS configuration, and PowerShell automation.

## Lab Environment

- Windows Server 2022
- Active Directory Domain Services
- DNS
- Oracle VirtualBox
- PowerShell
- CSV-based user provisioning

## Project Overview

The lab began with a fresh Windows Server installation configured as a domain controller named `DC01`.

A new Active Directory forest was created using the domain:

`lab.test`

The environment was organized into departmental organizational units for:

- IT
- HR
- Finance
- Operations
- Sales
- Management

Thirty users were created manually to practice the Active Directory user creation process.

The remaining users were provisioned using PowerShell and CSV data, bringing the environment to a total of 200 simulated employee accounts.

## Skills Demonstrated

- Windows Server installation and configuration
- Static IPv4 configuration
- Active Directory Domain Services deployment
- DNS configuration
- Domain controller promotion
- Organizational Unit creation
- Manual user provisioning
- PowerShell automation
- CSV-based bulk account creation
- Active Directory validation and user count verification

## 1. Windows Server Base Installation

A clean Windows Server 2022 installation was created in VirtualBox to serve as the foundation for the Active Directory environment.

![Windows Server Base Installation](Screenshots/01%20-%20Domain%20Controller%20Setup/01%20-%20Windows%20Server%20Base%20Installation.png)

## 2. DC01 Static IP Configuration

The domain controller was configured with the static IPv4 address `10.0.0.10` so client systems and domain services could reliably locate the server.

![DC01 Static IP Configuration](Screenshots/01%20-%20Domain%20Controller%20Setup/02%20-%20DC01%20Static%20IP%20Configuration.png)

