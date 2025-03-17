# SEER Stat inside of VMWware Fusion on a Mac M-Chip 
This guide provides instructions on setting up a Windows 11 virtual environment using VMware Fusion and configuring it specifically to work with the CDC SEER*Stat program on a Apple Mac with an M-processor. 

---

## Prerequisites

- VMware Fusion installed on macOS.
- Windows 11 ISO image. 
  - **Educational Users:** If you have an `.edu` email, you can obtain a free Windows license key from [Azure Education](https://azure.microsoft.com/free/students/).
- CDC SEER*Stat software.

---

## Step-by-Step Guide

### 1. Create Windows 11 Virtual Machine in VMware Fusion

1. Open VMware Fusion.
2. Click **File > New**.
3. Select **Install from disc or image** and click **Continue**.
4. Drag and drop your Windows 11 ISO image into the provided space, or browse and select the ISO file.
5. Click **Continue** and select **Windows 11** as the operating system.
6. Customize your VM resources as follows:
   - **RAM:** At least 4 GB (recommended 8 GB or more)
   - **Storage:** Minimum 64 GB
   - **Processors:** 2 cores or more recommended
7. Click **Finish** to create the VM.

---

### 2. Install Windows 11

1. Start the newly created VM in VMware Fusion.
2. Follow the on-screen instructions to install Windows 11.
3. When prompted for a product key, enter the key you received via Azure Education if applicable, or select "I don't have a product key" to activate later.
4. Complete the installation by following standard prompts and creating a user account.

---

### 3. Configure VMware Fusion Network Settings for SEER*Stat

- Ensure your VM is powered off.
- Select your Windows VM in VMware Fusion.
- Click **Settings > Network Adapter**.
- Choose **Bridged Networking (Autodetect)**.
- Close the settings to save the changes.

---

### 4. Configure Windows Firewall for SEER*Stat

To ensure SEER*Stat functions correctly, configure Windows Firewall:

- **Option A (Temporary for initial testing):**
  1. Open **Control Panel > System and Security > Windows Defender Firewall**.
  2. Select **Turn Windows Defender Firewall on or off**.
  3. Temporarily select **Turn off Windows Defender Firewall** for testing purposes.

- **Option B (Recommended, long-term):**
  1. Open **Control Panel > System and Security > Windows Defender Firewall**.
  2. Click **Allow an app or feature through Windows Defender Firewall**.
  3. Click **Change settings**, then **Allow another app**.
  4. Browse to the SEER*Stat executable (usually located in `C:\Program Files\SEERStat`) and allow both private and public network access.

---

### 5. Install and Run SEER*Stat

1. Download SEER*Stat from the [official SEER website](https://seer.cancer.gov/seerstat/).
2. Run the installer and follow the installation wizard **WITH ADMIN PERMISSIONS!**
3. Launch SEER*Stat to ensure it connects properly.

---

## Troubleshooting

- **Connectivity Issues:** Double-check the network adapter settings are set to **Bridged (Autodetect)**.
- **Firewall Problems:** Confirm SEER*Stat is allowed through the firewall.

---

## Additional Resources

- [VMware Fusion Documentation](https://docs.vmware.com/en/VMware-Fusion/index.html)
- [CDC SEER*Stat Support](https://seer.cancer.gov/seerstat/support/)

---

By following these steps, your Windows 11 environment in VMware Fusion should now be fully functional with SEER*Stat.

