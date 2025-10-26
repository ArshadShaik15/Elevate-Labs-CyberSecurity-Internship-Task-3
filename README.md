# Elevate-Labs-CyberSecurity-Internship-Task-3

<br>

### Task 3: Perform A Basic Vulnerability Scan On My PC

<br>

### **🎯 Objective:** <br>
To perform a basic vulnerability scan on my personal computer using a free tool (OpenVAS) or Nessus Essentials to identify and document common security weaknesses. <br>
<br>
<br>
### 🛠️ Lab Setup: <br><br>
### **📝 Note:**  <br>

<p align="left">I initially considered setting up an external virtualized environment using OpenVAS on a Kali Linux distribution to target a known-vulnerable machine (like Metasploitable). But the task assigned to me clearly states that i need to set up the scan target as my local machine IP or localhost for a basic vulnerability scan. So, Nessus Essentials was chosen for its effective, non-intrusive capabilities in conducting local, credentialed checks necessary for patch and configuration analysis.</p><br>

### Nessus Essentials (Ideal For Windows):
<p align="left">1. It uses a standard Windows Installer, which handles all service creation, dependencies, and pathing automatically. It is designed to be an <strong>install-and-run</strong> product.</p>
2. Nessus Essentials limits you to 16 scan targets, but offers the full, easy-to-use GUI on Windows. <br> 

### OpenVAS (Ideal For Linux/Kali): <br>
<p align="left">1. OpenVAS (Community Edition) is completely free and open-source with no IP limit, but requires a significant initial effort to set up and maintain.</p>
<p align="left">2. OpenVAS (specifically the Greenbone Vulnerability Management/GVM framework it's part of) has a complex architecture (scanner, manager, database).</p>
<p align="left">3. It's typically run as a pre-built virtual appliance or installed natively on Linux, which is a complicated process on Windows.</p>
<br>
<br>

### Step-1: Set Up Scan Target As Your Local Machine IP Or Localhost <br>

<br>  <img width="1502" height="632" alt="Screenshot 2025-10-25 171530" src="https://github.com/user-attachments/assets/5a77ba90-6680-4201-8d8a-0e21bdf02499" />  <br>
<br>
• Click the "New Scan" button in the top right corner of the dashboard.<br>
<br>
<br>  <img width="1501" height="829" alt="Screenshot 2025-10-25 171649" src="https://github.com/user-attachments/assets/469038b7-6968-48e2-8fc0-576f1ea2bb7a" />  <br>
<br>
• Choose the scan template that provides the most comprehensive check for vulnerabilities.<br>
• **"Basic Network Scan"** is the most common and robust option for a host PC.<br>
<br>
<br>  <img width="1501" height="792" alt="Screenshot 2025-10-25 135626" src="https://github.com/user-attachments/assets/15fe22b1-ac50-479e-a671-e938392bb86a" />  <br>
<br>
• Configure settings by filling the required fields:<br>

&nbsp;&nbsp; a. Give the scan a descriptive name - Basic Vulnerability Scan<br>
&nbsp;&nbsp; b. Description - My First PC Scan<br>
&nbsp;&nbsp; c. Targets - Enter the IP address that represents your computer<br>
&nbsp;&nbsp; d. Launch - Click "Save" and then, on the next screen, click the play button (▶) next to your **"Last Scanned"** to launch it.<br>
<br>
<br>  <img width="1919" height="433" alt="Screenshot 2025-10-25 140002" src="https://github.com/user-attachments/assets/6cb4abde-1483-4f7d-8201-fc9ccf1d8a70" />  <br>
<br>
<br>
### Step-2: Wait For Scan To Complete (May Take 30-60 Mins) <br>
<br>
<p align="left">• The scan will now run. This process is time-consuming. The scan can take 30-60 minutes or longer. Do not use your PC for heavy tasks during this time<br></p>
<br>  <img width="1919" height="486" alt="Screenshot 2025-10-25 140158" src="https://github.com/user-attachments/assets/1570a6b8-8e34-457e-b656-f705135a6658" /><br>
<br>  <img width="1915" height="468" alt="Screenshot 2025-10-25 141603" src="https://github.com/user-attachments/assets/646dc41f-f96a-45fc-9aff-6a66079a5caf" /><br>
<br>  <img width="1919" height="755" alt="Screenshot 2025-10-25 143103" src="https://github.com/user-attachments/assets/0fe1c46a-0736-42e8-8877-c421d391364b" /><br>
<br>
<p align="left">• My initial scan completed in a non-standard duration of 13 minutes, which was immediately flagged as an indicator of an incomplete assessment. Subsequent review confirmed that the initial authentication attempt to the target host had failed, preventing a deep system audit and resulting in a high percentage of false negatives (missed vulnerabilities).</p>

<p align="left">• Upon researching more, I found that my initial attempts to conduct a deep, credentialed vulnerability assessment failed due to authentication issues with the standard privileged service account, resulting in a scan that only identified informational findings and no Critical or High-severity vulnerabilities. To proceed with a comprehensive, uncompromised audit, the assessment methodology was temporarily adjusted.</p>

<p align="left">• Successfully authenticating to the Windows host required temporarily enabling the Built-in Administrator account to bypass User Access Control (UAC) limitations, achieving the critical <strong>'Auth: Pass'</strong> status for a deep assessment.</p>

<br> <img width="1919" height="792" alt="Screenshot 2025-10-25 172549" src="https://github.com/user-attachments/assets/2645159b-98b4-43a2-8375-dd75db7a9043" /><br>
<br>
<p align="left">• This change allowed me to obtain accurate results presented in this report, including one <strong>Critical</strong> and multiple <strong>High</strong>-severity findings. After successfully completing the scan, the Built-in Administrator account was immediately disabled to restore the system's default security posture and enforce the principle of least privilege.</p>

•  And as you can see, the scan was approximately 60 mins which is in indication that the scan was successful.<br>
<br>
<br>
### Step-3: Reviewing The Report For Vulnerabilities And Severity <br>

<br><img width="317" height="532" alt="Screenshot 2025-10-25 180011" src="https://github.com/user-attachments/assets/bc7f762b-df38-4e64-a43e-7ed74f1a7150" />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img width="313" height="548" alt="Screenshot 2025-10-25 180048" src="https://github.com/user-attachments/assets/93f67ed6-6821-4a40-b4a7-fbf471fc1113" />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img width="313" height="532" alt="Screenshot 2025-10-25 180120" src="https://github.com/user-attachments/assets/88a59cc7-5d8e-420d-be9e-9af798c03ced" /><br>
<br>  <img width="1272" height="885" alt="Screenshot 2025-10-25 175434" src="https://github.com/user-attachments/assets/09e56f8f-a8a3-4ff9-a9e9-54f604654c96" />  <br>
<br>  <img width="1275" height="285" alt="Screenshot 2025-10-25 175514" src="https://github.com/user-attachments/assets/c4b50ac1-a620-4482-a781-4b4769e1305d" />  <br>
<br>
• The final report identified **27 critical findings** (1 Critical, 19 High, 7 Medium). Prioritization was based on the combined CVSS and VPR scores.

## 📑 Critical Vulnerabilities (Top 3 Findings)

The following high-impact vulnerabilities require immediate patching or configuration change to mitigate the risk of system compromise:

| Vulnerability Title | Severity / CVSS v3.0 | 	VPR Score | Impact / Risk |
| :--- | :--- | :--- | :--- |
| **Docker Desktop < 4.44.3 Container Escape** | Critical / 9.3 | 9.9 | Allows a malicious container to break isolation and gain unauthorized access to the host operating system with elevated privileges. |
| **RARLAB WinRAR < 7.13 Directory Traversal** | High / 8.8 | 9.5 | An attacker can execute arbitrary code by crafting a malicious archive file, which can deploy malware to the Windows Startup folder upon extraction. |
| **WinVerifyTrust Signature Validation Mitigation** | High / 8.8 | 8.9 | A missing registry setting allows attackers to modify a signed executable to inject malicious code without invalidating the file's signature. |
<br>
<br>

### Step-4: Research Simple Fixes Or Mitigations For Found Vulnerabilities <br>

### 🧩 Vulnerability Assessment and Remediation

| Vulnerability Title | Severity | CVSS v3.0 | Impact / Risk (Your Research) | Remediation / Fix (Your Research) |
|----------------------|-----------|------------|--------------------------------|-----------------------------------|
| **1. Docker Desktop < 4.44.3 Container Escape** | **Critical** | 9.3 | Allows a malicious container to break isolation and gain unauthorized access to the host operating system with elevated privileges. | Upgrade Docker Desktop to version **4.44.3** or later. |
| **2. RARLAB WinRAR < 7.13 Directory Traversal (CVE-2025-8088)** | **High** | 8.8 | An attacker can execute arbitrary code by crafting a malicious archive file, which can deploy malware to sensitive directories like the **Windows Startup folder** upon extraction. | Update to **WinRAR version 7.13 Final** or later immediately. |
| **3. WinVerifyTrust Signature Validation (CVE-2013-3900 Mitigation)** | **High** | 8.8 | A missing registry setting allows attackers to modify an existing signed executable to inject malicious code without invalidating the file's signature. | Add and enable the registry key `EnableCertPaddingCheck` with a value of `1` in the appropriate **Wintrust\Config** paths. |
<br>

### **Summarizing My Learnings:** <br>

<p align="left">My assessment began by learning a core lesson in scanning: an initial, quick scan (e.g., 13 minutes) is often a false negative, signaling a failure to gain proper access due to security barriers like User Access Control (UAC), not a truly clean system. To ensure a complete audit, i documented the necessary step of temporarily enabling the Built-in Administrator account to bypass UAC limitations, which successfully achieved the crucial <strong>Auth:Pass</strong> status and correctly exposed a high-risk flaw: the Command Injection vulnerability (CVE-2025-55319) in Visual Studio Code, rated at CVSS 8.8. Finally, a process immediately followed by disabling the administrator account to maintain network security.</p>

### Vulnerability Assessment Process Summary

| Step | Action Taken | Security Rationale |
|------|---------------|--------------------|
| **Initial Scan Failure** | The first vulnerability scan was rapid (e.g., 13 minutes) and inconclusive, which was documented as being due to an authentication failure rather than a clean system. | This links the low-quality result directly to the technical issue, justifying the subsequent, deeper assessment. |
| **Authentication Strategy** | The team temporarily enabled the **Built-in Administrator** account to bypass **UAC limitations**, which successfully achieved the necessary **Auth: Pass** status for a deep, comprehensive audit. | This explains the why — to overcome Windows security features that block remote scanners, ensuring the audit was complete and accurate. |
| **Vulnerability Focus** | We confirmed the primary finding: **CVE-2025-55319**, a **Command Injection flaw** in *Microsoft Visual Studio Code Agentic AI* with a **CVSS score of 8.8**. | This established the high-priority fix target for the remediation team. |
| **Security Clean-up** | A critical detail was added: the Built-in Administrator account was immediately disabled post-scan (`net user administrator /active:no`). | This confirms adherence to the **Principle of Least Privilege**, proving the assessment was conducted responsibly. |
<br>
<br>

### **Conclusion:**<br>

This exercise proves that conducting an effective vulnerability assessment is two-fold: it requires overcoming common PC security blocks to find hidden risks, and it requires securing the resulting documentation to prevent a security solution from becoming a security problem. High-severity risks are often present, but masked, by standard PC security features like UAC, which is why a deep, authenticated audit is essential. We found a critical Command Injection vulnerability (CVSS 8.8) in a common piece of software, which is a powerful reminder that every application on your machine is a potential attack surface. The core defense for all users is not just rapid patching, but uncompromising adherence to the Principle of Least Privilege. Every account or application that gains temporary elevated access, such as a security tool or a routine update must be immediately demoted or restricted. By ensuring no user or process operates with more power than necessary, you dramatically limit the ability of any vulnerability, even a Critical one, to execute a complete system takeover.
