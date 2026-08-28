# Access-Based Enumeration (ABE)

Demonstrated **Access-Based Enumeration (ABE)** to hide shared folders from users who do not have permission to access them.

- Created a shared parent folder named **TestingABE** with two subfolders: **CSR** and **IT**.
- Configured permissions so **IT users could not access or see the CSR folder**, while **CSR users could not access or see the IT folder**.
- Configured the **TestingABE** share with read access at the share level and used **NTFS permissions** to grant access to the appropriate Security Groups.
- Disabled **NTFS permission inheritance** on both the CSR and IT subfolders to allow each folder to have its own independent permissions.
- Assigned the **CSR Security Group** permissions to the CSR folder and the **IT Security Group** permissions to the IT folder.
- Enabled **Access-Based Enumeration** through **Server Manager → File and Storage Services → Shares**.
- Tested the configuration by logging in as users from each department:
    - **IT user:** CSR folder was hidden.
    - **CSR user:** IT folder was hidden.

**Key takeaway:** ABE improves usability and security by preventing users from seeing shared folders they do not have permission to access, while NTFS permissions enforce the actual access control.

📁 **Screenshots:** See the `images` folder for a visual demonstration of the configuration and testing.