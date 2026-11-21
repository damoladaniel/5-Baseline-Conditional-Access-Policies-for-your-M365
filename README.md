# 5-Baseline-Conditional-Access-Policies-for-your-M365
In this Lab. I will demonstrate how to setup a Modern Multifactor authentication method and use it to configure 5 important Conditonal Access Policies

-----------------------
## Project Summary

Conditional Access is one of the highest-value security controls in a Microsoft environment, and most security baselines treat it as essential.
- Most breaches now start with a stolen or phished credential, not a firewall exploit. Conditional Access is how you control what a valid login can actually do.
- MFA stops the large majority of account takeover attempts, and Conditional Access is how you enforce it consistently, rather than leaving it to per-user settings that get missed. Passwords are not enough
- Cyber Essentials Plus, ISO 27001 and most cyber insurers now expect enforced MFA and access controls, and Conditional Access is the standard way to evidence that.

## Objectives
- Configure a Modern Authentication Method and Authentication Strength
- Create 5 Baseline Conditonal Access Policies for Entra ID tenants or M365 tenants
## Tools & Environment
- Entra ID
- Admin Break Glass accounts

## First things first
I configured an Authentication Strength 
Authentication Methods -> Authentication Strengths -> New Authentication

Selected:
##### Phishing-resistant MFA
- Windows Hello for Business
- Passkeys (FIDO2)

##### Multifactor Authentication
- Multifactor Aunthenticator (Phone Sign-in)
- Temporary Access Pass (One-time Use)
- Password + Microsoft Authenticator (Push Notification)

<br></br>

<img width="1612" height="866" alt="Screenshot 2026-11-21 122707" src="https://github.com/user-attachments/assets/db309a84-93d7-4041-8419-e23ef628cfcb" />

## Condtional Access 1: All Users - All Apps: Require Strong MFA
