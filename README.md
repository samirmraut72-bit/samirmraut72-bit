Connected Business IT Environment

I am building practical IT infrastructure labs to understand how the main technology components of a real business work together.

The goal of these projects is to cover the major areas an organisation depends on every day: networking, users and devices, servers, Active Directory, DNS, Group Policy, cloud identity, endpoint management, security, business applications and troubleshooting.

Rather than treating each topic as a separate lab, I am building them as one connected environment so I can understand the full flow of IT inside an organisation.

## How the projects connect

```mermaid
%%{init: {'theme':'base','themeVariables':{
  'background':'#ffffff',
  'primaryColor':'#000000',
  'primaryTextColor':'#ffffff',
  'primaryBorderColor':'#ffffff',
  'lineColor':'#ffffff',
  'secondaryColor':'#000000',
  'tertiaryColor':'#000000',
  'fontFamily':'Arial'
}}}%%
flowchart TD

    U["Users & Business Devices<br/>Staff, Doctors, Admin<br/>PCs, Phones, Printers"]

    N["Network Infrastructure<br/>VLANs, Switching, Routing<br/>OSPF, HSRP, DHCP, ACLs"]

    W["Windows Infrastructure<br/>Windows Server, AD DS<br/>DNS, Group Policy"]

    I["Identity & Device Management<br/>Entra ID, MFA<br/>App Roles, Intune"]

    A["Business Application<br/>MedSecure Clinical Platform"]

    S["Security & Troubleshooting<br/>RBAC, Port Security<br/>Logging, Testing"]

    U --> N
    N --> W
    W --> I
    I --> A

    S --- N
    S --- W
    S --- I
    S --- A
