# Active Directory Administration Labs

Hands-on labs covering Windows Server Active Directory, Group Policy, departmental file access, and identity synchronization with Microsoft Entra ID.

Each project includes configuration notes and screenshots of the results.

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
| [OUs, Users and Security Groups](01%20-%20Creating%20OUs%2C%20Security%20Groups%2C%20Users%20and%20their%20passwords) | Creating a departmental OU, adding users, and assigning security group memberships |
| [Group Policy Configuration](02%20-%20Creating%2C%20linking%20and%20testing%20GPOs) | Creating and linking a GPO, configuring security filtering, and verifying a user restriction |
| [File and Folder Permissions](03%20-%20file%20permissions) | Configuring SMB share and NTFS permissions, mapping drives, and testing permitted and denied access |
| [Windows Autologon and Browser Startup](04%20-%20Creating%20a%20service%20account) | Configuring a dedicated interactive account, automatic sign-in, and fullscreen browser launch |
| [Access-Based Enumeration](05%20-%20Access-Based%20Enumeration%20%28ABE%29) | Configuring departmental folder visibility, NTFS inheritance, and testing with different users |
| [Hybrid Identity with Entra ID](06%20-%20Hybrid-Identity%20%28Entra%20ID%20Sync%29) | Preparing UPNs, deploying Entra Connect Sync, configuring OU filtering, and verifying synchronized identities |

## Lab Environment

- VMware Workstation
- Windows Server 2025 domain controller: `DC01`
- Windows 11 Enterprise client VM: `Client01`
- Active Directory domain: `Ben.local`
- Active Directory Domain Services and DNS
- Group Policy Management
- SMB file sharing and NTFS permissions
- Microsoft Entra ID and Entra Connect Sync for the hybrid identity lab

Individual project READMEs describe the configuration used for each exercise.

## Verification

Testing included:

- Confirming user membership in departmental security groups
- Verifying that a targeted user received a Control Panel restriction
- Accessing an authorized departmental share and confirming access was denied to another
- Comparing shared-folder visibility between IT and CSR users
- Restarting a client to verify automatic sign-in and browser startup
- Confirming that selected AD users appeared in Entra ID with on-premises synchronization enabled

## Related PowerShell Project

I also built an **AD User Access Report** that retrieves account status, password information, OU location, and group memberships. It returns structured output that can be exported to CSV.

The project includes successful lookups, nonexistent-user error handling, and CSV export verification.

[View the AD User Access Report](https://github.com/behnamMasoumi/Powershell-Automation-Lab/tree/main/03-AD-User-Access-Report)

## Skills Practiced

- AD user, group, and OU administration
- Group Policy linking and security filtering
- Share and NTFS permissions
- Access-Based Enumeration
- Windows client configuration
- Alternate UPN suffixes
- Microsoft Entra Connect Sync
- Password Hash Synchronization configuration
- OU-based synchronization filtering
- PowerShell queries, DNS diagnostics, and connectivity checks
