# Kiosk Service Account & Automated Kiosk Configuration

Configured a Windows client to automatically log in using a dedicated **service account** and launch a browser in fullscreen kiosk-style mode.

- Created a dedicated **Service Accounts OU** in Active Directory and created a **Kiosk Service** user within it.
- Used **Microsoft Sysinternals Suite**, a collection of advanced Windows administration and troubleshooting utilities, commonly used by IT professionals for system diagnostics, automation, security, and configuration. Used **Autologon** to configure automatic sign-in for the kiosk account.
- Configured **Google Chrome** to automatically open `www.amazon.com` at startup.
- Added the Chrome shortcut to the Windows **Startup folder** using `shell:startup`, ensuring Chrome launches automatically after login.
- Configured Chrome to launch in **fullscreen mode**, creating a kiosk-style user experience with minimal user interaction.
- Restarted the client VM and successfully verified the complete workflow: **automatic login → Chrome launch → Amazon opens → fullscreen display**.

📁 **Screenshots:** 14 step-by-step images are available in the `images` folder.