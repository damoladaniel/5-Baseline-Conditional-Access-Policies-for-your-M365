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

Name: Modern MFA

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

## Condtional Access 1:
Name: **All Users - All Apps: Require Strong MFA**
Assignments:
- Users: Include All Users, ***(Excluse break glass and admin accounts)***
- Grant: Modern MFA (Previously Created MFA Method)
- Enable Policy: On
------------------------------

<img width="1250" height="856" alt="Screenshot 2026-11-21 122821" src="https://github.com/user-attachments/assets/d14601ed-3d7c-40ae-9ddc-bd046110da31" />

-----------------------------

<img width="1844" height="870" alt="Screenshot 2026-11-23 091021" src="https://github.com/user-attachments/assets/038c1ae7-207a-4ec4-8193-248f538ef631" />

-----------------------------

## Conditional Access 2:

The policy blocks protocols that dont support MFA e.g POP, IMAP. Legacy POP and IMAP protocols traditionally use Basic Authentication (username and password), which cannot prompt for multi-factor authentication (MFA) or enforce modern sign-on policies.

Name: **All Users - Legacy Auth Clients: Block Access**
Assignments: 
- Users: Include All Users, ***(Excluse break glass and admin accounts)***
- Condtions -> Client Apps -> Configure (YES) -> Selcet Legacy Authentication Clients (Exchange ActiveSync Cleints & Other Clients)
- Grant : Block Access
- Enable Policy: On

<img width="1140" height="403" alt="Screenshot 2026-11-23 095509" src="https://github.com/user-attachments/assets/efa29d2b-240d-47b2-8615-588bf6f2fc58" />

------------

<img width="1844" height="782" alt="Screenshot 2026-11-23 095558" src="https://github.com/user-attachments/assets/19a354be-f31d-4ed9-a151-27f20e8d071b" />

------------

<img width="850" height="738" alt="Screenshot 2026-11-23 095609" src="https://github.com/user-attachments/assets/c8f8596b-6102-49f9-b7d3-912d8764edfe" />

------------

<img width="1871" height="865" alt="Screenshot 2026-11-23 095730" src="https://github.com/user-attachments/assets/9298d90d-4051-4456-b5e6-f678208dc6e7" />

------------

<img width="1900" height="890" alt="Screenshot 2026-11-23 095805" src="https://github.com/user-attachments/assets/457a225e-3c6e-435c-ad05-e7cb6eb8c6bd" />

------------

<img width="689" height="870" alt="Screenshot 2026-11-23 095831" src="https://github.com/user-attachments/assets/4fafe216-60ac-4de8-ab01-79f103ece397" />






