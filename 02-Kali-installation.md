🐉 Kali Linux Installation on Oracle VirtualBox

A step-by-step guide to installing and configuring Kali Linux inside Oracle VM VirtualBox for cybersecurity learning, ethical hacking, and penetration testing.

![VirtualBox](https://img.shields.io/badge/VirtualBox-7.2-blue)
![Kali Linux](https://img.shields.io/badge/Kali-Linux-blue)
![Cybersecurity](https://img.shields.io/badge/Domain-Cybersecurity-red)
![Status](https://img.shields.io/badge/Status-Completed-success)

📌 1. Introduction

Kali Linux is a Debian-based Linux distribution designed for cybersecurity professionals, penetration testers, and security researchers.

It includes various tools for:

- Network Security Testing
- Vulnerability Assessment
- Web Application Security Testing
- Digital Forensics
- Wireless Security Testing
- Penetration Testing

Purpose: To install Kali Linux inside Oracle VM VirtualBox and create a controlled virtual cybersecurity lab environment.

💻 2. System Requirements

Before installing Kali Linux, make sure your computer meets the following recommended requirements:

Component| Recommended
Operating System| Windows 10/11
RAM| 8 GB or more
Processor| 64-bit CPU
Virtualization| Intel VT-x / AMD-V
Free Storage| 40 GB or more
VirtualBox| Installed

Note: Allocate resources according to your host computer's available hardware.

📥 3. Download Kali Linux ISO

Follow these steps to download Kali Linux:

1. Open the official Kali Linux website.
2. Navigate to the Downloads section.
3. Select the Installer Images option.
4. Download the 64-bit Installer ISO.
5. Save the ISO file on your computer.

Official Download: https://www.kali.org/get-kali/

"Kali Linux Download" (screenshots/Kali-Download.png)

🖥️ 4. Open Oracle VirtualBox

1. Launch Oracle VM VirtualBox.
2. Click on the New button.
3. Enter the virtual machine name: "Kali Linux".
4. Select the folder where the VM files will be stored.
5. Select the downloaded Kali Linux ISO image.
6. Choose Linux as the operating system type.
7. Select Debian (64-bit) as the version, if required.

"VirtualBox New VM" (screenshots/Kali-New-VM.png)

⚙️ 5. Configure Virtual Machine Hardware

Configure the virtual machine according to your computer's available resources.

Memory (RAM)

- Recommended: 4 GB (4096 MB) or more.
- Do not allocate all your computer's RAM to the VM.

Processors (CPU)

- Recommended: 2 CPU cores or more.
- Keep sufficient CPU resources available for the host operating system.

"Hardware Configuration" (screenshots/Kali-Hardware-Configuration.png)

💾 6. Create Virtual Hard Disk

1. Select Create a Virtual Hard Disk Now.
2. Choose VDI (VirtualBox Disk Image).
3. Select Dynamically Allocated.
4. Set the disk size to 40 GB or more.
5. Click Finish.

"Virtual Disk Configuration" (screenshots/Kali-Virtual-Disk.png)

🌐 7. Configure Network Settings

1. Select your Kali Linux virtual machine.
2. Open Settings.
3. Navigate to Network.
4. Select Adapter 1.
5. Enable Network Adapter.
6. Select NAT for basic internet connectivity.

Note: NAT is suitable for basic installation and updates. For an isolated multi-VM cybersecurity lab, consider Host-Only networking or an appropriately configured internal network.

"Network Configuration" (screenshots/Kali-Network-Configuration.png)

🚀 8. Start Kali Linux Installation

1. Select the Kali Linux VM.
2. Click Start.
3. Wait for the Kali Linux boot menu.
4. Select Graphical Install.
5. Press Enter.

"Kali Boot Menu" (screenshots/Kali-Boot-Menu.png)

🌍 9. Configure Language, Location and Keyboard

During installation:

1. Select your preferred language.
2. Select your country or location.
3. Choose your keyboard layout.
4. Continue to the next installation step.

"Language Configuration" (screenshots/Kali-Language-Configuration.png)

👤 10. Configure User Account

1. Enter a hostname for your Kali system.
2. Configure the domain name if required; otherwise, leave it blank.
3. Enter your full name.
4. Create a username.
5. Set a strong password.
6. Confirm the password.

Security Tip: Never share your Kali Linux password or store it in public repositories.

"User Configuration" (screenshots/Kali-User-Configuration.png)

🗂️ 11. Disk Partitioning

For a beginner installation:

1. Select Guided - Use Entire Disk.
2. Select the virtual hard disk created for Kali Linux.
3. Choose the recommended partition layout.
4. Review the partition changes.
5. Confirm writing changes to disk.

⚠️ Important: Make sure you select only the VirtualBox virtual hard disk. Do not select your physical computer's actual hard disk.

"Disk Partitioning" (screenshots/Kali-Disk-Partitioning.png)

📦 12. Install the Base System

1. The installer will begin installing the Kali Linux base system.
2. Wait for the installation process to complete.
3. Select the required software components.
4. Continue with the installation.

"Installation Progress" (screenshots/Kali-Installation-Progress.png)

🔧 13. Install GRUB Bootloader

1. When prompted, choose Yes to install the GRUB bootloader.
2. Select the virtual hard disk as the bootloader installation device.
3. Wait for the bootloader installation to complete.

"GRUB Installation" (screenshots/Kali-GRUB-Installation.png)

🔄 14. Complete Installation and Reboot

1. Wait for the installation to finish.
2. Select Continue or Reboot.
3. If the VM boots into the installer again, remove or detach the ISO from the virtual optical drive.
4. Start the virtual machine again.

"Installation Complete" (screenshots/Kali-Installation-Complete.png)

🔐 15. Login to Kali Linux

1. Wait for the Kali Linux login screen.
2. Enter the username created during installation.
3. Enter your password.
4. Press Enter to access the desktop.

"Kali Login" (screenshots/Kali-Login.png)

🔄 16. Update Kali Linux

After logging in, open the Terminal and execute:

Update package information:

sudo apt update

Upgrade installed packages:

sudo apt full-upgrade -y

Remove unnecessary packages:

sudo apt autoremove -y

Note: Keep your Kali Linux system updated to receive security fixes and software updates.

🧰 17. Install VirtualBox Guest Additions

Guest Additions can improve display integration, mouse integration, and other VM features.

Open the Kali Linux terminal:

sudo apt install -y virtualbox-guest-x11

Then reboot:

sudo reboot

Verify that the features work correctly after restarting.

🔍 18. Verify Kali Linux Installation

Open the terminal and execute the following commands:

Check Kali Linux version:

cat /etc/os-release

Check kernel version:

uname -r

Check IP address:

ip addr

Check network connectivity:

ping -c 4 8.8.8.8

If the commands work as expected, your Kali Linux installation is ready for further configuration.

"Kali Desktop" (screenshots/Kali-Desktop.png)

🧪 19. Next Steps

After successfully installing Kali Linux, you can continue with:

- Basic Linux Commands
- Linux File System
- Networking Fundamentals
- Nmap Installation and Usage
- Subdomain Enumeration
- Web Application Security Testing
- OWASP Top 10
- Burp Suite Setup
- Metasploit Framework
- Cybersecurity Lab Configuration

🛠️ 20. Common Installation Issues

Issue| Possible Solution
VM does not start| Check hardware virtualization settings
Black screen| Check VM display settings and graphics controller
No internet| Verify VirtualBox network adapter settings
Slow performance| Adjust RAM and CPU allocation
ISO boots repeatedly| Remove the ISO after installation
Screen resolution issue| Install Guest Additions

📸 21. Screenshots Directory

Store all installation screenshots in the following directory:

screenshots/
│
├── Kali-Download.png
├── Kali-New-VM.png
├── Kali-Hardware-Configuration.png
├── Kali-Virtual-Disk.png
├── Kali-Network-Configuration.png
├── Kali-Boot-Menu.png
├── Kali-Language-Configuration.png
├── Kali-User-Configuration.png
├── Kali-Disk-Partitioning.png
├── Kali-Installation-Progress.png
├── Kali-GRUB-Installation.png
├── Kali-Installation-Complete.png
├── Kali-Login.png
└── Kali-Desktop.png

⚠️ 22. Security Disclaimer

This virtual lab is created for educational purposes, cybersecurity learning, and authorized penetration testing.

Always obtain proper authorization before testing any network, website, application, or computer system.

Never perform security testing against systems without permission.


📚 References

- Kali Linux Official Website: https://www.kali.org/
- Kali Linux Documentation: https://www.kali.org/docs/
- Kali Linux Downloads: https://www.kali.org/get-kali/
- Oracle VirtualBox: https://www.virtualbox.org/



Platform: Oracle VM VirtualBox

Operating System: Kali Linux

Purpose: Ethical Hacking and Penetration Testing Lab

Author: Cybersecurity Lab Project
