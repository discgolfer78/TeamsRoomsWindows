Deploying Microsoft Teams Rooms on Windows for InfoComm 2026
Author: Mark Layton, The Avail Group

This repository contains a public, anonymized deployment guide for building and deploying Windows-based Microsoft Teams Rooms (MTR) devices with Teams Rooms Pro, Microsoft Intune, Microsoft Entra ID, Windows Autopilot, and Autologin.
The original tenant and user-specific values have been anonymized:
Tenant/domain prefix: `abc123`
Admin user prefix: `Admin`
Example tenant domain: `abc123.onmicrosoft.com`
Example admin account: `Admin@abc123.onmicrosoft.com`
> \\\*\\\*Security note:\\\*\\\* Do not publish real passwords, serial numbers, tenant names, customer names, PKIDs, or production device identifiers in this repository.
---
Scenario
This guide covers deploying Windows-based Microsoft Teams Rooms devices for InfoComm 2026.
Example device scope:
Microsoft Teams Rooms on Windows
Teams Rooms Pro licensing
Windows Autopilot self-deploying mode
Teams Rooms Autologin
Microsoft Intune enrollment
Microsoft Entra ID dynamic device groups
LAPS for local administrator password management
Exchange Online room mailbox configuration
Conditional Access exclusions for Teams Rooms resource accounts
Teams Rooms Pro Management Portal remote access
Example hardware:
Shure IntelliMix Foundation Compute IMXCPU5 running Microsoft Teams Rooms on Windows
Shure IntelliMix Bar Pro
Logitech Windows-based Microsoft Teams Rooms device
---

High-level deployment flow
Register the Windows MTR device in Partner Center by using the PKID from the device packaging.
Assign a Partner Center group tag that starts with `MTR-`.
Create an Entra ID dynamic device group for Teams Rooms devices.
Deploy the Teams Rooms app update tool / MTRP Provisioning Tool with Intune.
Create and assign an Enrollment Status Page profile.
Create and assign a self-deploying Windows Autopilot profile.
Create and assign a LAPS policy.
Create the Teams Rooms resource account.
Assign the Microsoft Teams Rooms Pro license.
Configure the Exchange Online room mailbox.
Set the mailbox time zone.
Disable password expiration for the resource account.
Exclude the Teams Rooms resource account from MFA-based Conditional Access policies.
Validate the resource account with the Teams Rooms sign-in test.
Assign the resource account to the device in the Teams Rooms Pro Management Portal for Autologin.
Hand off the device to the onsite technician for physical deployment.
---
Microsoft documentation
Primary Microsoft documentation used for this deployment:
Windows Autopilot and Autologin for Teams Rooms on Windows
Autopilot partner registration
Autopilot registration for Teams Rooms partners
Create a group for Teams Rooms devices
Deploy the Teams Rooms app update tool
Create a Windows Autopilot ESP profile
Create and assign a self-deploying Windows Autopilot profile
LAPS management policy settings
LAPS for Teams Rooms
Create and configure resource accounts for Teams Rooms
Configure mailbox properties for Teams Rooms
Mailbox time zone settings
Conditional Access and compliance for Teams Rooms
Remotely access Teams Rooms
Teams Rooms device sign-in test
---
