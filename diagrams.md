## Storage Account Enumeration -  NetSPI

![](ppt/media/image1.png "Content Placeholder 4")

## Slide 2

Logs and Events from IT and Cloud Resources

Security Tools – Alerts/Incidents

Microsoft Defender for Cloud, 

Microsoft Defender for Endpoint

Azure Monitor

L1 SOC Analyst

(SOP)

L2 SOC Analyst

L3 SOC Analyst

Evaluates the case and escalates further for analysis

## Slide 3

Session manager

‘smss.exe’

Windows Initialization Process

‘wininit.exe’

Client Server Runtime Subsystem

‘cssrss.exe’

Boot initialization

It starts system services

Service control manager

‘ services.exe ’

Local security authority

‘lsass.exe’

Local session manager

‘lsm.exe’

After handling system processes  Session manager  again starts  CSRSS

Session 0

for system processes

Client Server Runtime Subsystem

‘cssrss.exe’

Session 1

for User processes

Windows logon process

‘winlogon.exe’

Local session manager

‘LogonUI.exe’

Starts login process

LogonUI.exe  takes credentials and passes them to  lsass.exe

‘UserInit.exe’

Executables initiated by Userinit.exe

- Explorer.exe : Desktop, Taskbar, Explorer, Start menu
- cmd.exe:  Executes logon scripts (batch files)
- Powershell.exe:  Runs  PowerShell scripts
- Wscript.exe/Cscript.exe:  Executes  VBScript or JavaScript-based logon scripts .
- Gpupdate.exe:  Ensures that  Group Policy settings  are applied.
- Net.exe:  Used for mapping network drives (e.g., net use X:  \\server\share ). 
- Rundll32.exe:  Can be used to  load DLLs for specific startup tasks .
- Taskhost.exe:  Loads DLL-based services from the registry (similar to svchost.exe).
- Msiexec.exe:  Handles installation of startup applications via . msi  installers. 

Handles user authentication UI before passing control to  userinit.exe

cmd.exe

cmd.exe

Winlogon.exe calls Userinit.exe after successful authentication

Windows Authentication

## Kerberos Authentication 

Kerberos is the default authentication method used for  Windows 11, Windows Server 2022, and Windows Server 2019.

## Security Posture

<div class="smartart cycle6" layout="cycle6">

</div>

## Security Posture

<div class="smartart cycle6" layout="cycle6">

</div>

## Defense in Depth Architecture

<div class="smartart venn2" layout="venn2">

</div>

Identity and Access Management

Network Firewall

DDoS Protection

Antimalware

Patching

Patching

Network Security Group

Secure File Transfer

Secure Remote Access

Secure Coding

Secure DevOps

DAST and SAST

Data Encryption

Data Classification

Data loss prevention

## Slide 8

<div class="smartart orgChart1" layout="orgChart1">

**Network security**

- Business processes
- Support
- Sponsorship
- Culture
- Acceptance

**Information security**

- Scope & Objective
- Requirement definition
- Testing
- Technical processes
- Overall technical performance
- Technology employed
- User interfaces
- Technology scaling
- Safety, security and reliability

**End user security**

- Financing
- Subcontracts
- Vendor Stability
- General contract
- Contractor experience
- Legal

**Operational security**

- Weather
- Political
- Legislative
- Unforeseeable circumstances
- Regulatory
- Pressure from outside groups

**Project Risk**

- End user security
- Operational security
- Application security
- Network security
- Disaster security
- Information security

**Disaster security**

- Interdependencies
- Project management
- Communication
- Project resources

**Application security**

- Authentication
- Application Security testing
- Authorization
- Encryption
- Logging

</div>

## Cloud Access Security Broker

![Computer](ppt/media/image2.png "Graphic 4")

![Computer](ppt/media/image4.png "Graphic 5")

Corporate Device

BYOD

CASB

Visibility

Threat protection

Data Security

Compliance

Enterprise integration

Redirected end user and Administrator traffic to cloud service traffic

Enterprise integration

![Cloud](ppt/media/image6.png "Graphic 31")

![Cloud](ppt/media/image6.png "Graphic 32")

![Cloud](ppt/media/image6.png "Graphic 33")

IaaS

SaaS

PaaS

Redirected traffic

API Access

## RACI Matrix

<div class="smartart LinedList" layout="LinedList">

**Responsible**

- Individuals responsible for actually performing a task. 
- You  will review the policies, perform testing, document deficiencies and generate a report.
- You as the IT auditor are responsible for conducting the audit. 

**Informed**

- The Audit Committee needs to be informed about the audit progress and the results, as they have a vested interest in the organization's audit practice.
- Individuals kept in the loop but are not directly involved in the task. 

**Accountable**

- Individuals ultimately answerable for the completion of the task or deliverable. 
- The  Lead Auditor / Chief Audit Executive (CAE) will be accountable for ensuring the overall audit completion and issuing the audit report.

**Consulted**

- Individuals who provide input and are consulted before a task is executed. 
- The  Cyber & Risk Management team will be consulted because they have valuable insights into the technical aspects

</div>

## Slide 11

![](ppt/media/image8.png "Picture 1")

 

Here is a diagram that shows how to implement Sentinel in a hybrid environment:

https://learn.microsoft.com/en-us/azure/architecture/hybrid/hybrid-security-monitoring

 

## Access control in Azure and Microsoft Entra

Different objects at different scopes are controlled in different ways. 

Microsoft Entra Tenant

App

Group

User

Service 

principal

Device

- Entra Roles
- Graph API Permissions
- Object scoped roles
- Explicit Ownership

Root Management Group

Management Group

Management Group

Subscriptions

Resource Groups

VMs

Key Vault

DB

Blobs

- Azure Admin Roles
- Attribute based access controls
- Keys, Secrets, and Certificates

Certain objects like key vaults have their own permission model specific to that object 

- How much fun is that?  

There is no one click in Azure where you can see all effective permissions of these objects
