<p align="center">
  <img src="https://i.imgur.com/zq5ZlZQ.png" alt="Cloud Engineer Academy Logo" width="250"/>
</p>

# ☁️ Cloud Engineer Academy – Project Curls (Week 1)

This project is part of the **Cloud Engineer Academy** curriculum under **Week 1: Cloud Fundamentals**.  
It demonstrates how to use the command line to install tools, make HTTP GET requests, and analyze HTTP response headers using the `curl` command-line utility.

---

## 🧭 Project Overview

The **Curl Requests Project** focuses on understanding how clients and servers communicate over the web using HTTP.  
By the end of this exercise, I learned how to:
- Install and verify command-line tools like `curl`
- Perform and analyze HTTP GET requests
- Troubleshoot and fix environment issues (like WSL2 virtualization)
- Create documentation directly from within Linux using Markdown

---

## 🧱 Environment Setup

**Operating Systems Used:**
- Windows 11 (Host)
- Ubuntu 22.04 LTS (via Windows Subsystem for Linux 2)

**Tools & Technologies:**
- PowerShell (for WSL setup)
- Ubuntu CLI
- `curl` (for HTTP requests)
- `nano` (for documentation)
- Task Manager (for virtualization verification)

---

<h2>Step 1 – WSL2 Installation Error</h2>

When first attempting to install Ubuntu, an error message appeared:  
> “WSL2 is not supported with your current machine configuration.  
> Please enable the ‘Virtual Machine Platform’ optional component and ensure virtualization is enabled in the BIOS.”

**Actions Taken**
- Opened PowerShell as Administrator  
- Ran initial `wsl --install` command  
- Identified virtualization not enabled in BIOS  

📸 *Screenshot Placeholder (01-wsl2-error.png)*

---

<h2>Step 2 – Fixing the Installation</h2>

After enabling virtualization features in Windows and BIOS, I re-ran the commands:


wsl --install --no-distribution
wsl --install -d Ubuntu
---

<h2>Step 3 – Verifying Virtualization</h2>

Once the BIOS settings were corrected, I verified that **virtualization was enabled** via **Task Manager → Performance → CPU tab**.

**Result:**  
- Virtualization status confirmed as “Enabled” ✅

📸 *Screenshot Placeholder (03-virtualization-enabled.png)*

---

<h2>Step 4 – Ubuntu Installation Success</h2>

After confirming virtualization, Ubuntu was successfully installed in WSL.

**Actions Taken**
- Launched Ubuntu from Windows Terminal  
- Observed setup completion message  
- Reached the Linux shell prompt  

📸 *Screenshot Placeholder (04-ubuntu-installed.png)*

---

<h2>Step 5 – First Login and User Setup</h2>

Created a new Linux user account (`danso`) and confirmed access to the terminal.

**Result:**
- Password successfully created  
- Verified prompt switched to user session  

📸 *Screenshot Placeholder (05-ubuntu-first-login.png)*

---

<h2>Step 6 – Installing and Testing curl</h2>

Installed `curl` for performing HTTP requests within the Ubuntu environment.


sudo apt update
sudo apt install curl -y
curl --version

