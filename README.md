# Guide to Activating Windows 11 Pro for Free

## Why Upgrade to Windows 11 Pro?
Upgrading to Windows 11 Pro unlocks additional features such as:
- **BitLocker Encryption** for enhanced security
- **Remote Desktop Hosting** to access your PC from anywhere

## Can You Upgrade to Windows 11 Pro for Free?
Yes! You can switch from almost any edition to Pro at no cost.

## Already Using Windows 11 Pro (Unactivated)?
If you already have Windows 11 Pro but it is unactivated, skip to the [Activation Steps](#activating-windows-11-pro).

---
## Getting Started
### Opening Command Prompt as Administrator
1. Press **Windows + R** to open the Run dialog box.
2. Type **cmd.exe** and press **Ctrl + Shift + Enter**.
3. Click **Yes** when prompted by User Account Control (UAC).

You should now see an Administrator Command Prompt window.

---
## Running Essential Commands
### Step 1: Clearing Previous Keys
Enter the following commands one by one, pressing **Enter** after each:
```cmd
slmgr.vbs /upk  # Uninstall existing product key
slmgr.vbs /cpky  # Clear product key from registry
slmgr.vbs /ckms  # Remove any existing KMS configuration
```
Click **OK** after each confirmation message.

### Step 2: Checking Upgrade Compatibility
To check if your edition supports an upgrade to Pro, run:
```cmd
DISM /online /Get-TargetEditions
```
If **Professional** is listed, you can proceed with the upgrade.

### Step 3: Running the Windows 11 Pro Installer
Run the following commands to configure necessary services and initiate the upgrade:
```cmd
sc config LicenseManager start= auto & net start LicenseManager
sc config wuauserv start= auto & net start wuauserv
changepk.exe /productkey VK7JG-NPHTM-C97JM-9MPGT-3V66T
exit
```
Once the process starts, wait for it to reach **100%**. If an error occurs, simply restart your PC.

After rebooting, Windows 11 Pro should be installed. However, it will not yet be activated.

---
## Activating Windows 11 Pro
### Step 4: Running Activation Commands
1. Open **Command Prompt as Administrator** (repeat the previous steps).
2. Enter these commands one by one:
```cmd
slmgr /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX  # Install product key
slmgr /skms kms8.msguides.com  # Set KMS server
slmgr /ato  # Activate Windows
```
3. Wait for the activation process to complete.

Now, your Windows 11 Pro is fully activated! 🎉 You can verify this by checking **Settings > System > About**.

---
## Video Tutorial
For a step-by-step visual guide, watch this tutorial:
[![Video Tutorial](https://img.youtube.com/vi/Q132Tr40z_8/0.jpg)](https://www.youtube.com/watch?v=Q132Tr40z_8)

---
## Final Notes
I hope this guide helps! If you have any questions, feel free to reach out.

Author: **Nazrul Islam**  
Contact: **mhdnazrul511@gmail.com**

