# **File & Folder Permissions**

Demonstrated how **NTFS permissions** and **network share permissions** can be used to control access to folders based on Security Groups.

- Created two folders: **ITFolder** and **CSRFolder**.
- **NTFS permissions** control access to files and folders within the Windows file system.
- **Share permissions** control access when a folder is accessed **over the network** (for example, through `\\DC01\ITFolder`).
- Configured **ITFolder** to grant the **IT-Department Security Group** Full Control.
- On the client VM, mapped `\\DC01\ITFolder` to a drive letter and successfully accessed it using an account that belonged to the IT Security Group.
- Configured **CSRFolder** to allow access only to the **CSR Security Group**.
- Attempted to map `\\DC01\CSRFolder` using the IT account. Access was correctly denied because the account was not a member of the CSR Security Group.

**Key takeaway:** In a real-world environment, permissions are typically assigned to **Security Groups rather than individual users**, making access control easier to manage as employees join or leave departments.

📁 **Screenshots:** See the `images` folder for a visual demonstration of the permissions and access tests.