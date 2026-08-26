# Creating a Group Policy Object

Created and applied a **Group Policy Object (GPO)** to restrict Control Panel access for a specific security group.

- Verified that **Group Policy Management** was installed on the Windows Server Domain Controller.
- Created a new GPO named **Control Panel Restrictions**.
- Linked the GPO to the **Users OU**, since the policy targets users.
- Configured the policy under **User Configuration → Administrative Templates → Control Panel → Prohibit access to Control Panel and PC settings**.
- Added the **CSR Security Group** to **Security Filtering** so the policy only targets the intended users.
- Under **Delegation → Advanced**, removed **Apply Group Policy** permission from **Authenticated Users** to prevent the policy from applying broadly.
- Tested the configuration on the Windows client VM using **Justin**, a member of the CSR Security Group.
- Ran `gpupdate /force` to refresh Group Policy and confirmed the restriction was successfully applied when Control Panel access was blocked.

📁 **Screenshots:** See the `images` folder for a visual demonstration of the configuration and testing.