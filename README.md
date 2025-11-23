# Smart India Hackathon Workshop - Operating System
### Date : 23-11-2025 
### Register Number: 212224230225
### Name: Raviprasath K
## Problem Title
SIH1446 - Developing a GUI based hardening script for Ubuntu operating system with flexibility to cater for organisational security policies## Problem Description

**Background**: Hardening of an operating system involves implementation of security measure to make the system compliant with the security policies of the organization. The procedure for hardening should be intuitive to allow ease of use by personnel with minimal IT skills. The goal of this problem statement is to generate a script which is undertakes hardening of Ubuntu OS using an GUI based approach. During the hardening process, the user should have the flexibility to make settings based on the organisations IT security policy provision like blocking ssh, usb, ToR etc. The grading of tool will be based on hardening functions implemented, attention to user experience and flexibility to take user settings. Developer should remember that security is of utmost importance.

**Organization**: National Technical Research Organisation,(NTRO)

**Category**: Software

## Ubuntu Hardening Scripts - Quick Reference

## Repository 1: konstruktoid/hardening

A comprehensive hardening script for Ubuntu servers that applies security configurations following best practices.

### 1. Setting GRUB Password

**Command:**
```bash
grub-mkpasswd-pbkdf2
```

**Explanation:**  
This command generates an encrypted password for your GRUB bootloader. It's an important security measure that prevents unauthorized users from editing boot parameters or accessing recovery mode. The command will prompt you to enter a password twice, then output an encrypted hash that you'll need to add to your GRUB configuration.

### 2. Running the ubuntu.sh Script

**Command:**
```bash
sudo bash ubuntu.sh
```

**Explanation:**  
This executes the main hardening script with root privileges. Before running it, make sure you've configured the `ubuntu.cfg` file with your preferences (especially the CHANGEME variable). The script will apply numerous security settings, install security tools, configure the firewall, and harden SSH access. Always test in a non-production environment first since these changes are not reversible.

---

## Repository 2: conduro/ubuntu

A streamlined hardening script specifically designed for Ubuntu 20.04 Server to optimize and secure systems running web applications.

### 1. Downloading Conduro

**Command:**
```bash
wget -O ./install.sh https://condu.ro/install.sh
```

**Explanation:**  
This downloads the installation script from the Conduro website and saves it as `install.sh` in your current directory. The `-O` flag specifies the output filename. This is a one-liner that fetches the script directly from their server, making it easy to get started quickly.

### 2. Changing install.sh Permissions

**Command:**
```bash
chmod +x ./install.sh
```

**Explanation:**  
This makes the install.sh script executable. By default, downloaded files don't have execute permissions for security reasons. The `+x` flag adds execute permission, allowing you to run the script. After this, you can execute it with `sudo ./install.sh` to begin the hardening process.
