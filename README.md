# How to Activate Windows 11 Pro for Free

## Why Upgrade to Windows 11 Pro?
Windows 11 Pro offers additional features such as:
- **BitLocker Encryption** for enhanced security.
- **Remote Desktop Hosting** to access your device over the internet.

## Can I Upgrade from Any Edition to Pro?
Yes! You can upgrade from almost any Windows edition to Pro for free.

## Already Using Windows 11 Pro but Not Activated?
If you already have Windows 11 Pro installed but it is not activated, skip directly to [this step](https://gist.github.com/Minionguyjpro/d913b3931e844ad8ad9a758a4aca4b63#activating-windows-pro).

---

## Getting Started
### Step 1: Open Command Prompt as Administrator
1. Press **Windows + R** to open the Run dialog box.
2. Type `cmd.exe` and press **Ctrl + Shift + Enter** to open Command Prompt as an administrator.
3. Click **Yes** when prompted.

---

## Step 2: Run the Required Commands
### **Reset Licensing Configuration**
Run the following commands one by one, clicking **OK** after each:
```
slmgr.vbs /upk
slmgr.vbs /cpky
slmgr.vbs /ckms
```

### **Check Upgrade Compatibility**
Run this command to check if your Windows edition supports an upgrade to Pro:
```
DISM /online /Get-TargetEditions
```
If "Professional" appears in the list, you can proceed with the upgrade.

### **Run the Windows Pro Installer**
Copy and paste the following commands into Command Prompt:
```
sc config LicenseManager start= auto & net start LicenseManager
sc config wuauserv start= auto & net start wuauserv
changepk.exe /productkey VK7JG-NPHTM-C97JM-9MPGT-3V66T
exit
```
Wait for the process to reach 100%. If you encounter an error, simply click **Exit**, restart your PC, and allow the update process to complete.

---

## Step 3: Activate Windows 11 Pro
### **Final Activation Commands**
Reopen Command Prompt as Administrator using **Windows + R**, typing `cmd.exe`, and pressing **Ctrl + Shift + Enter**. Then enter the following:
```
slmgr /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX
slmgr /skms kms8.msguides.com
slmgr /ato
```
## Step 4: Activate Windows 11 Pro and MS Office all products.
Here are the steps to use the command `irm https://get.activated.win | iex` to activate Windows and Office:

Step 1: Open PowerShell as Administrator. You must have admin rights to run the activation script.  
Step 2: Copy the command
```
irm https://get.activated.win | iex
```
Step 3: Paste the command into the PowerShell window and press Enter.  
Step 4: The script downloads the activation script from the provided URL and verifies its integrity.  
Step 5: The script will then attempt to activate your Windows operating system and Microsoft Office products using the embedded activation method.  
Step 6: Restart your computer to complete the activation process.  
Step 7: Verify activation status by going to System Settings for Windows activation or opening your Office app to check the activation status.  

Once completed, Windows 11 Pro will be activated. You can verify this in **Settings > System > About**.

---

## Video Tutorial
For a step-by-step walkthrough, check out this video tutorial:
[![Video Tutorial](https://img.youtube.com/vi/Q132Tr40z_8/0.jpg)](https://www.youtube.com/watch?v=Q132Tr40z_8)

---

## Need Help?
If you have any questions, feel free to reach out via email: **[mhdnazrul511@gmail.com]** or leave a comment.

Enjoy your upgraded Windows 11 Pro experience! 🚀

