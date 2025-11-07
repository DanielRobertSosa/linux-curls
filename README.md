<p align="center">
  <img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/a1c2a591-717a-434a-95b9-af1ad27a8952" />

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

<p align="center">
<img width="1038" height="550" alt="Screenshot 2025-11-06 142319" src="https://github.com/user-attachments/assets/4473a9b0-e715-4071-90e5-2a14e3151dbe" />


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

<p align="center">
<img width="1072" height="724" alt="Screenshot 2025-11-06 145751" src="https://github.com/user-attachments/assets/83f2a083-d7fa-40c5-a3d8-bd0fec84a2d1" />


---

<h2>Step 4 – Ubuntu Installation Success</h2>

After confirming virtualization, Ubuntu was successfully installed in WSL.

**Actions Taken**
- Launched Ubuntu from Windows Terminal  
- Observed setup completion message  
- Reached the Linux shell prompt  

<p align="center">
<img width="1718" height="947" alt="Screenshot 2025-11-06 150657" src="https://github.com/user-attachments/assets/fb1ebee4-4f3b-4352-ac48-7968be8158e5" />

---

<h2>Step 5 – First Login and User Setup</h2>

Created a new Linux user account (`danso`) and confirmed access to the terminal.

**Result:**
- Password successfully created  
- Verified prompt switched to user session  

<p align="center">
<img width="986" height="453" alt="Screenshot 2025-11-06 151631" src="https://github.com/user-attachments/assets/f9871adc-bc83-49c7-adeb-d3db5f3a4743" />

---

<h2>Step 6 – Installing and Testing curl</h2>

Installed `curl` for performing HTTP requests within the Ubuntu environment.


sudo apt update
sudo apt install curl -y
curl --version

---

<h2>Step 7 – Performing HTTP Requests with curl</h2>

Executed real HTTP requests using the `curl` command to fetch data and analyze HTTP response headers.

<h2>Results</h2>
-  HTML successfully retrieved from example.com
-  Local HTML file saved as example.html
-  Verified HTTP 200 OK response

📸 Screenshot Placeholder

-  (07-curl-requests.png)

<h2>Step 8 – Documenting the Project in Ubuntu</h2>

Used the nano text editor to create and edit a README file directly inside Ubuntu.
This step demonstrates documenting technical work entirely from the Linux terminal using Markdown.

<h2>Results</h2>

  -  Successfully opened and edited README.md using nano
  -  Practiced Markdown formatting and documentation structure
  -  reinforced Linux file editing workflow (Ctrl+O → Enter → Ctrl+X)
  -  verified README.md file saved inside /home/<user> directory

<h2>Objective Achieved</h2>
  -  Practiced professional documentation habits inside Linux
  -  Strengthened Markdown writing and version-control workflow
  -  Finalized project summary with all commands, screenshots, and outcomes

📸 Screenshot Placeholder
  -  (08-readme-nano.png)

✅ Project Results / Validation

-  WSL2 configured and virtualization verified
-  Ubuntu successfully installed and running under Windows
-  curl installed, tested, and verified through real HTTP requests
-  HTTP response headers retrieved and analyzed
-  Markdown documentation created directly within Linux

🎯 Lessons Learned / Conclusion

-  Learned to install and verify CLI tools such as curl and nano
-  Understood how HTTP GET requests retrieve webpage data
-  Practiced using the command line to test network connections
-  Strengthened Windows ↔ Linux integration skills via WSL2 configuration
-  Built confidence documenting projects directly inside Ubuntu




