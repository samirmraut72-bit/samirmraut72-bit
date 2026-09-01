Connected Business IT Environment

I am building practical IT infrastructure labs to understand how the main technology components of a real business work together.

The goal of these projects is to cover the major areas an organisation depends on every day: networking, users and devices, servers, Active Directory, DNS, Group Policy, cloud identity, endpoint management, security, business applications and troubleshooting.

Rather than treating each topic as a separate lab, I am building them as one connected environment so I can understand the full flow of IT inside an organisation.

## How the projects connect

```mermaid
%%{init: {'theme':'base','themeVariables':{
  'background':'#008000',
  'primaryColor':'#cfefff',
  'primaryTextColor':'#ffffff',
  'primaryBorderColor':'#9ed8f5',
  'lineColor':'#7aa7c7',
  'secondaryColor':'#cfefff',
  'tertiaryColor':'#cfefff',
  'fontFamily':'Arial'
}}}%%
flowchart TD
    USERS["Users & Business Devices<br/>Staff, Doctors, Admin,<br/>PCs, Phones, Printers"]
    NETWORK["Network Infrastructure<br/>VLANs, Switching, Routing,<br/>OSPF, HSRP, DHCP, ACLs"]
    SYSTEMS["Windows Infrastructure<br/>Windows Server, AD DS,<br/>DNS, Group Policy"]
    IDENTITY["Identity & Device Management<br/>Entra ID, MFA,<br/>App Roles, Intune"]
    APP["Business Application<br/>MedSecure Clinical Platform"]
    SECURITY["Security & Troubleshooting<br/>RBAC, Port Security,<br/>Logging, Testing"]

    USERS --> NETWORK
    NETWORK --> SYSTEMS
    SYSTEMS --> IDENTITY
    IDENTITY --> APP

    SECURITY --- NETWORK
    SECURITY --- SYSTEMS
    SECURITY --- IDENTITY
    SECURITY --- APP
