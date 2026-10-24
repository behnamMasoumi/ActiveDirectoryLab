# Active Directory Administration Labs

Hands-on labs covering Windows Server Active Directory, Group Policy, departmental file access, hybrid identity, and internal web services using IIS.

Each project includes configuration notes and screenshots demonstrating the implementation and results.

## Featured Project: Hybrid Identity

Connected an existing Active Directory domain to Microsoft Entra ID using **Microsoft Entra Connect Sync**.

The project covers:

- Adding an alternate UPN suffix and preparing test users
- Checking DNS health, domain membership, and Microsoft endpoint connectivity
- Configuring Password Hash Synchronization
- Limiting synchronization to a dedicated OU
- Verifying synchronized users in Entra ID
- Inspecting a successful delta synchronization operation

The documented results demonstrate directory synchronization. Cloud sign-in and password-change propagation were not separately verified.

[View the Hybrid Identity project](06%20-%20Hybrid-Identity%20%28Entra%20ID%20Sync%29)

## Projects

| Project | What I Practiced |
| --- | --- |
| [OUs, Users and Security Groups](01%20-%20Creating%20OUs%2C%20Security%20Groups%2C%20Users%20and%20their%20passwords) | Creating departmental OUs, adding users, and assigning security group memberships |
| [Group Policy Configuration](02%20-%20Creating%2C%20linking%20and%20testing%20GPOs) | Creating and linking GPOs, configuring security filtering, and verifying user restrictions |
| [File and Folder Permissions](03%20-%20file%20permissions) | Configuring SMB shares and NTFS permissions, mapping drives, and testing permitted and denied access |
| [Windows Autologon and Browser Startup](04%20-%20Creating%20a%20service%20account) | Configuring a dedicated interactive account, automatic sign-in, and fullscreen browser launch |
| [Access-Based Enumeration](05%20-%20Access-Based%20Enumeration%20%28ABE%29) | Configuring departmental folder visibility, NTFS inheritance, and testing access with different users |
| [Hybrid Identity with Entra ID](06%20-%20Hybrid-Identity%20%28Entra%20ID%20Sync%29) | Preparing UPNs, deploying Entra Connect Sync, configuring OU filtering, and verifying synchronized identities |
| [IIS Intranet Deployment with AD Authentication](07%20-%20IIS-Intranet-Deployment-AD-Authentication) | Hosting HR and IT websites on IIS, configuring internal DNS and hostname bindings, and restricting access using Windows Authentication and AD security groups |

## Lab Environment

- VMware Workstation
- Windows Server 2025 domain controller: `DC01`
- Windows 11 Enterprise client VM
- Active Directory Domain Services (AD DS)
- DNS and Group Policy Management
- SMB file sharing and NTFS permissions
- Microsoft Entra ID and Entra Connect Sync
- Internet Information Services (IIS) 10
- Windows Authentication and IIS URL Authorization

*Individual project READMEs describe their respective domain configurations, implementation steps, and testing results.*

## Verification

Testing across the projects included:

- Confirming user membership in departmental Active Directory security groups
- Verifying that targeted users received Group Policy restrictions
- Accessing authorized departmental shares and confirming unauthorized access was denied
- Comparing shared-folder visibility between departmental accounts using Access-Based Enumeration
- Restarting a client to verify automatic sign-in and browser startup
- Confirming that selected Active Directory users synchronized successfully with Microsoft Entra ID
- Verifying internal DNS resolution for departmental HR and IT websites
- Testing Windows Authentication and access restrictions using authorized and unauthorized domain accounts
- Confirming that multiple IIS websites operated on the same server IP address and HTTP port using separate hostname bindings

## Related PowerShell Project

I also built an **AD User Access Report** that retrieves account status, password-related information, OU location, and security group memberships. It returns structured output that can be exported to CSV.

The project includes successful lookups, nonexistent-user error handling, and CSV export verification.

[View the AD User Access Report](https://github.com/behnamMasoumi/Powershell-Automation-Lab/tree/main/03-AD-User-Access-Report)

## Skills Practiced

- Active Directory user, group, and OU administration
- Group Policy configuration, linking, and security filtering
- SMB sharing and NTFS permissions
- Access-Based Enumeration (ABE)
- Windows client configuration
- Microsoft Entra Connect Sync and hybrid identity
- Password Hash Synchronization configuration
- OU-based synchronization filtering
- Windows Server IIS website hosting and administration
- Internal DNS configuration and name resolution
- IIS hostname bindings and default documents
- Windows Integrated Authentication
- Active Directory security group-based website authorization
- PowerShell queries, DNS diagnostics, and connectivity testing
