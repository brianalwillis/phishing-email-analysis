<h1 = align=center>𝙿𝙷𝙸𝚂𝙷𝙸𝙽𝙶 𝙴𝙼𝙰𝙸𝙻 𝙰𝙽𝙰𝙻𝚈𝚂𝙸𝚂</h1>

<p align="center">
<img width="1008" height="584" alt="Untitled Diagram drawio (2)" src="https://github.com/user-attachments/assets/908268b9-c6e7-47e3-8406-38c7eebc538a" />
</p>

<h2 = align=center><code>NIST 800-61</code> <em>Computer Security Incidient Handling Guide</em></h2>

<h3 = aligh=cener>Preparation | <code>Detection and Analysis</code> | Containment, Eradication, and Recovery | Post-Incident Activity</h3>

---

## 🛠️ TECHNOLOGY & PLATFORMS UTILIZED

- `VirtualBox:`  
  Served as the primary virtualization platform for hosting isolated virtual machines. Enabled secure handling and analysis of live phishing email samples without risk to the host system.

- `Windows VM:`  
  Used as a simulated user endpoint for testing how phishing emails appear to typical users.

- `Kali Linux VM:` 
  Acted as the primary analysis machine. Used to open and investigate live phishing email samples, inspect links and attachments, and perform forensic tasks using built-in and custom tools.

- `Mozilla Thunderbird:` 
  Configured as the email client to view `.eml` files and live phishing samples. Provided an interface to inspect headers, body content, and attachments in a realistic user context.

- `Bitdefender Email Protection:`  
  Used to demonstrate how phishing emails are detected and handled from both the end-user and analyst perspectives. Showcased how suspicious emails are flagged within the user interface and how threat details (e.g., malicious attachments or URLs) are reported through Bitdefender’s security console for further analysis.

## 🔍 EMAIL ANALYSIS TOOLS

- [`EML Analyzer`](https://eml-analyzer.herokuapp.com/#/):  
  A web tool used to parse `.eml` files and extract detailed header information, detect anomalies, and identify common phishing indicators.

- [`VirusTotal`](https://www.virustotal.com/gui/home/upload):  
  Used to analyze suspicious email attachments, domains, IPs, and URLs to detect malware, phishing, and other threats.

- [`Blue Coat Site Review`](https://sitereview.bluecoat.com/#/):  
  Used to check the domain reputation and categorization of embedded URLs in phishing emails.

- [`URLScan.io`](https://urlscan.io/):  
  Performed sandbox scans of phishing URLs to observe redirect chains, scripts, and web content in a controlled environment.

- [`MXToolbox - Email Header Analyzer`](https://mxtoolbox.com/EmailHeaders.aspx):  
  Used to decode and analyze email headers, identify forged sender addresses, detect IP mismatches, and trace delivery paths.

- [`AbuseIPDB`](https://www.abuseipdb.com/): 
  Checked sender IPs against a global abuse database to identify addresses associated with spam, malware, or phishing activity.

---

## 🎯 OBJECTIVE

The objective of this project was to analyze `real-world phishing emails` in a controlled virtual environment to better understand common `attack vectors`, `social engineering` techniques, and the technical `indicators of compromise` (IOCs) used in malicious emails. By leveraging various tools—including `email clients`, `threat intelligence` platforms, and `endpoint protection` software—the project aimed to simulate both end-user and analyst perspectives. The goal was to enhance email threat detection skills, practice forensic analysis, and evaluate the effectiveness of modern email security solutions in identifying and mitigating phishing threats.

---

## PREPARATION

### Step 1: Setup the `Virtualization Platform`

- [`VirtualBox:`](https://www.virtualbox.org/) Served as the primary virtualization platform for hosting isolated virtual machines.
  
- [`Kali Linux`](https://www.kali.org/) Virtual Machine: Acted as the primary analysis machine. Used to open and investigate live phishing email samples, inspect links and attachments, and perform forensic tasks using built-in and custom tools.
  
- [`Windows`](https://www.microsoft.com/en-ca/software-download/windows10) Virtual Machine: Used as a simulated user endpoint for testing how phishing emails appear to typical users.

---

### Step 2: Download [`Thunderbird`](https://www.thunderbird.net/en-US/) to Kali Linux

- `Mozilla Thunderbird:` Configured as the email client to view `.eml` files and live phishing samples. Provided an interface to inspect headers, body content, and attachments in a realistic user context.

<img width="1177" height="752" alt="Lab 1" src="https://github.com/user-attachments/assets/88feaff8-3b69-41e3-98f8-c9807f63f714" />

---

### Step 3: Download `Phishing Email` Samples to Kali Linux

- [`Phishing Pot:`](https://github.com/rf-peixoto/phishing_pot/tree/main) The Phishing Pot is a collection of real phishing samples collected via honeypots. The purpose of this repository is to provide a reliable database for researchers and developers of detection solutions.

<img width="601" height="505" alt="Lab 4" src="https://github.com/user-attachments/assets/bf824170-990b-457d-b00a-56803ac3b1d6" /></br>

***WARNING:** Do **NOT** download or open live phishing email samples directly on your physical (host) machine. These emails often contain malicious links or attachments that can compromise your system. Always analyze phishing samples within a **secure virtual environment** (e.g., VirtualBox or VMware) that is isolated from your main network to prevent accidental infection or data loss.*

--- 

# *`Sample-1.eml`*

<img width="696" height="747" alt="sample-10 drawio" src="https://github.com/user-attachments/assets/54be26cd-0d04-4a81-8d89-9da2e460e7b2" /></br>

This phishing email impersonates the `Microsoft account team` and is sent from a spoofed address: `no-reply@access-accsecurity.com`. It claims to notify the recipient about unusual sign-in activity from `Russia/Moscow` using `Windows 10` and `Firefox`, with the IP address `103.225.77.255`.

### 🚩 Red Flags:
- The `reply-to` address is a personal Gmail account `sotrecognized@gmail.com`, which is not associated with Microsoft.
- The `Report The User` and `click here` links both open a pre-filled email to the attacker's Gmail address `sotrecognized@gmail.com`, attempting to trick the user into engaging.
- The domain `access-security.com` is suspicious and unrelated to official Microsoft services.

*Summary: This email phishing attempt is designed to harvest personal information or manipulate the user into responding, potentially exposing them to further attacks.*

## EMAIL ANALYSIS TOOLS:

### `EML Analyzer`

<img width="1125" height="297" alt="Lab 7" src="https://github.com/user-attachments/assets/fe0406bb-9f6c-482f-8f09-41ae6c5e593c" />

<img width="1325" height="372" alt="Lab 9" src="https://github.com/user-attachments/assets/0c146bae-601e-40c1-870c-a7579106dd55" />

<img width="1127" height="95" alt="Lab 10" src="https://github.com/user-attachments/assets/0f91906a-848f-4628-8aab-3021e5d17876" />

<img width="920" height="217" alt="Lab 11" src="https://github.com/user-attachments/assets/862ffa2a-ed83-4f43-a914-d433a1b54985" />

### `VirusTotal`

<img width="1311" height="601" alt="Lab 12" src="https://github.com/user-attachments/assets/5dcca6f8-2683-4c39-b6d3-f0d7e8c8ccaf" /></br>

This URL points to a hidden 1×1 pixel image hosted on `thebandalisty.com`, likely used as a tracking pixel to monitor when the phishing email is opened. Its presence indicates an attempt to confirm the recipient’s activity or identity, which is a common tactic in phishing campaigns.

---

# *`Sample-2.eml`*

<img width="768" height="762" alt="Untitled Diagram drawio (1)" src="https://github.com/user-attachments/assets/dd6afc22-14f1-4f7b-ac9a-08feed01771f" />

This phishing email, spoofed as coming from Hulu Membership `noreply@membershiphulu.com`, falsely claims that the recipient’s Hulu TV membership has expired and offers a `free 90-day extension` as part of a `fake loyalty program`. It includes a prominent `EXTENDED FOR FREE` button designed to lure users into clicking.

### 🚩 Red Flags:
- A suspicious sender domain not officially tied to Hulu.
- Urgent, reward-based language (`extend for free`) to manipulate the recipient.
- A fake `unsubscribe` link, which may lead to malicious sites or confirm a valid email address for future targeting.

*Summary: This is a typical phishing attempt aimed at harvesting personal or payment information under the guise of a membership renewal.*

## EMAIL ANALYSIS TOOLS:

### `EML Analyzer`

<img width="1120" height="292" alt="Lab 47" src="https://github.com/user-attachments/assets/eca3fc6a-e3aa-41f3-92db-deaad28957d4" />

<img width="1164" height="94" alt="Lab 48" src="https://github.com/user-attachments/assets/d19feb3c-bb5c-4487-9c71-810058c5be90" />

### `VirusTotal`

<img width="1310" height="562" alt="Lab 44" src="https://github.com/user-attachments/assets/87fc37b9-0338-43bc-9aed-475a6d34eb61" />

### `Blue Coat Site Review`

<img width="493" height="442" alt="Lab 45" src="https://github.com/user-attachments/assets/3a88a863-c66d-45d2-ba82-0c9dfd47a50a" />

---

# *`Sample-3.eml`*

<img width="774" height="759" alt="Untitled Diagram drawio (2)" src="https://github.com/user-attachments/assets/4fe567f9-eae5-435b-9684-86ab3b2e12f6" /></br>

This phishing email, disguised as a `McAfee` renewal notice from `noreply@customersupport.mcafee.com`, falsely warns the recipient that their antivirus subscription has expired and uses fear tactics like `WE ARE NOT RESPONSIBLE if you are HACKED` to provoke immediate action. The reply-to address (`z1ZaafVbZV@sunsy.co.uk`) is unrelated to McAfee and is a strong indicator of phishing.

### 🚩 Red Flags:
- Spoofed sender domain and unrelated reply-to address from `sunsy.co.uk`.
- Uses scare tactics and urgency to pressure the user into clicking (`suspended`, `hacked`, `expires today`).
- Promotes a fake `70% renewal discount` to bait the user into engaging with malicious links.
- References to `account ID`, `username`, and `subscription status` to create a false sense of legitimacy.

*Summary: This email is a phishing attempt designed to steal personal or payment information by impersonating McAfee and manipulating the user through fear-based messaging..*

## EMAIL ANALYSIS TOOLS:

### `VirusTotal`

<img width="1309" height="515" alt="Lab 51" src="https://github.com/user-attachments/assets/98e7a8fe-2414-4f01-a7ea-467820ab045b" />

### `Blue Coat Site Review`

<img width="380" height="444" alt="Lab 50" src="https://github.com/user-attachments/assets/4b0dd795-cbcc-4d24-af89-79f84c68ec01" />

---

# Email Protection with `Bitdefender`

There are many `email filtering` and protection tools available to help individuals and organizations defend against phishing attacks. For this project, I chose to test `Bitdefender` to evaluate its effectiveness in detecting and handling suspicious emails.

<img width="885" height="630" alt="Lab 59" src="https://github.com/user-attachments/assets/3c5e0fd5-88ab-4fe4-9d31-03fe233abd00" /></br>

I set up a test Gmail account (`brianalyst1@gmail.com`) on the `Windows 10` virtual machine and integrated it with `Bitdefender`. From the analyst’s perspective, Bitdefender’s interface provides visibility into all scanned emails for each account, categorizing them as safe or dangerous based on threat detection. This feature allows for quick assessment and response to potentially malicious messages.

<img width="884" height="632" alt="Lab 67" src="https://github.com/user-attachments/assets/a58e68c6-fbac-4b43-a7cf-2959c5acf06a" /></br>

From the end user’s perspective within the email account, `Bitdefender` automatically flags incoming messages with visual indicators: a red tag for `dangerous` emails and a green tag for `safe` emails. This immediate, color-coded labeling helps users quickly identify potential threats without needing technical expertise.

<img width="597" height="161" alt="Lab 64" src="https://github.com/user-attachments/assets/ef99bcbd-a917-4154-b04f-cb4362c9a91d" />

---

*The purpose of this project was to safely analyze real-world phishing emails in a controlled virtual environment to understand how they operate, identify key indicators of phishing, and evaluate the effectiveness of security tools like Bitdefender in detecting and flagging threats. It aimed to provide insight from both the end-user and analyst perspectives to improve email threat awareness and response.*

**Created By:** `Briana Willis`  
**Date:** `2025-07-17`  
**Time:** `8:31 UTC`
















