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

## 3. Active Directory and DNS Installed

Active Directory Domain Services and DNS were installed on `DC01`, preparing the server to function as the domain controller for the lab environment.

![Active Directory and DNS Installed](Screenshots/01%20-%20Domain%20Controller%20Setup/03%20-%20DC01%20Active%20Directory%20and%20DNS%20Installed.png)

## 4. Active Directory Domain Created

The Windows Server was promoted to a domain controller and a new Active Directory forest was created using the domain `lab.test`.

![Active Directory Domain Created](Screenshots/01%20-%20Domain%20Controller%20Setup/04%20-%20Active%20Directory%20Domain%20Created.png)

## 5. Department OU Structure

A parent organizational unit named `Company Users` was created, with separate department OUs for IT, HR, Finance, Operations, Sales, and Management.

![Department OU Structure](Screenshots/02%20-%20Active%20Directory%20Structure/01%20-%20Department%20OU%20Structure.png)

## 6. 30 Users Manually Created

Thirty user accounts were created manually, with five users placed into each department OU. This provided hands-on practice with account creation before moving to automation.

![30 Users Manually Created](Screenshots/02%20-%20Active%20Directory%20Structure/02%20-%2030%20Users%20Manually%20Created.png)

## 7. 200 Active Directory Users Created

After validating the manual provisioning process, additional fictional employee accounts were created using CSV data and PowerShell automation. The environment was expanded to a total of 200 users.

![200 Active Directory Users Created](Screenshots/03%20-%20User%20Provisioning/01%20-%20200%20Active%20Directory%20Users%20Created.png)

## 8. PowerShell User Count Verification

PowerShell was used to verify the final number of Active Directory accounts and confirm that the department totals matched the planned organizational structure.

![PowerShell User Count Verification](Screenshots/03%20-%20User%20Provisioning/02%20-%20PowerShell%20User%20Count%20Verification.png)

## Results

The lab resulted in a working Windows Server 2022 domain controller running Active Directory Domain Services and DNS.

The `lab.test` domain was organized into six departmental organizational units and populated with 200 simulated employee accounts.

User provisioning was completed through a combination of manual administration and PowerShell automation using CSV data.

## What I Learned

- How to install and configure Windows Server 2022
- How to configure a static IPv4 address for a domain controller
- How to install Active Directory Domain Services and DNS
- How to promote a Windows Server system to a domain controller
- How to create and organize users using organizational units
- How to manually provision Active Directory accounts
- How to use CSV files and PowerShell to automate bulk account creation
- How to check for duplicate usernames before provisioning accounts
- How to verify Active Directory user counts using PowerShell
