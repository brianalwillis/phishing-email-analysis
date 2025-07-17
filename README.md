<h1 = align=center>𝙿𝙷𝙸𝚂𝙷𝙸𝙽𝙶 𝙴𝙼𝙰𝙸𝙻 𝙰𝙽𝙰𝙻𝚈𝚂𝙸𝚂</h1>

<p align="center">
<img width="1008" height="584" alt="Untitled Diagram drawio (2)" src="https://github.com/user-attachments/assets/908268b9-c6e7-47e3-8406-38c7eebc538a" />
</p>

## 🛠️ TECHNOLOGY & PLATFORMS UTILIZED

- **`VirtualBox:`**  
  Served as the primary virtualization platform for hosting isolated virtual machines. Enabled secure handling and analysis of live phishing email samples without risk to the host system.

- **`Windows 10 VM:`**  
  Used as a simulated user endpoint for testing how phishing emails appear to typical users.

- **`Kali Linux VM:`**  
  Acted as the primary analysis machine. Used to open and investigate live phishing email samples, inspect links and attachments, and perform forensic tasks using built-in and custom tools.

- **`Mozilla Thunderbird:`**  
  Configured as the email client to view `.eml` files and live phishing samples. Provided an interface to inspect headers, body content, and attachments in a realistic user context.

- **`Bitdefender Email Protection:`**  
  Used to demonstrate how phishing emails are detected and handled from both the end-user and analyst perspectives. Showcased how suspicious emails are flagged within the user interface and how threat details (e.g., malicious attachments or URLs) are reported through Bitdefender’s security console for further analysis.

## 🔍 EMAIL ANALYSIS TOOLS

- **[`EML Analyzer`](https://eml-analyzer.herokuapp.com/#/):**  
  A web tool used to parse `.eml` files and extract detailed header information, detect anomalies, and identify common phishing indicators.

- **[`VirusTotal`](https://www.virustotal.com/gui/home/upload):**  
  Used to analyze suspicious email attachments, domains, IPs, and URLs to detect malware, phishing, and other threats.

- **[`Blue Coat Site Review`](https://sitereview.bluecoat.com/#/):**  
  Used to check the domain reputation and categorization of embedded URLs in phishing emails.

- **[`URLScan.io`](https://urlscan.io/):**  
  Performed sandbox scans of phishing URLs to observe redirect chains, scripts, and web content in a controlled environment.

- **[`MXToolbox - Email Header Analyzer`](https://mxtoolbox.com/EmailHeaders.aspx):**  
  Used to decode and analyze email headers, identify forged sender addresses, detect IP mismatches, and trace delivery paths.

- **[`AbuseIPDB`](https://www.abuseipdb.com/):**  
  Checked sender IPs against a global abuse database to identify addresses associated with spam, malware, or phishing activity.
