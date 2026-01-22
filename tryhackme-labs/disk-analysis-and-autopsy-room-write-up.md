# Disk Analysis And Autopsy - TryHackMe Write-Up

**Date:** January 22nd 2026

**Room Link:** [https://tryhackme.com/room/autopsy2ze0]

**Overview:** Simulated manual forensics analysis of a disk image to recover artifacts and answer investigative questions using Autopsy.

## Situation
I was presented with a disk image ('Hasan.E01') containing potential evidence of suspicious activities such as user accounts, installed programs and media files. This mirrors real world scenarios in digital investigations like examining seized devices in cyber crime cases.

## Task
The objective is to open the case, run ingest modules adn explore artifacts (media files, installed programs etc) and answer 15 questions to reconstruct events and dentify indicators of compromise.

## Actions
1. Opened the provided case and verified the data source (sie, timezone)
2. Noted that ingest modules had already been run (Keyword search, Timeline, etc.), which allowed to immediately begin exploring artifacts
3. Analysed installed programs and found credential-dumping tools (Mimikatz LaZagne) - Potential IOCs for compromise.
4. Explored media gallery and extracted content/metadata
5. Performed keyword searches for exploits, YARA files and other terms, revealing relevant hits (e.g., MS-NRPC, Zerologon, exploit archive).

**Tools Used:** Autopsy 4.18.0

## Result
Successfully recovered deleted files, extracted metadata, and identified high-risk tools (Mimikatz, LaZagne) and exploit references. All 15 questions answered without needing timeline generation, but noted its value for future sequence reconstruction 

**Key Learning Points:**
- Pre-run ingest in labs highlights how automation streamlines real investigations, freeing analysis for interpretation
- Timelines and keyword searches are crucial for event reconstruction
- Tools like Mimikatz and LaZagne flag potential credential theft in compromise cases.
- Media gallery allows a rapid triage of visual evidence (critical in time-sensitive cases)

## Screenshots:
**Opening Case Database** <img width="855" height="706" alt="opening-case-database" src="https://github.com/user-attachments/assets/0993eddc-5ab4-4d41-8f5b-96a9550c4e81" />

**Data Sources Overview**<img width="970" height="762" alt="reviewing-data-sources" src="https://github.com/user-attachments/assets/7578bc08-ed2f-4a63-a32e-1c22e67a2ebd" />

**Operating System User Accounts Table**<img width="764" height="773" alt="os-user-accounts" src="https://github.com/user-attachments/assets/b94740d5-dc31-4c0a-a728-a2c568a42a0b" />

**Installed Programs – Mimikatz Entry**<img width="1919" height="775" alt="mimikatz-installed" src="https://github.com/user-attachments/assets/d3b6dc5a-6239-48bf-be28-ad7e85249f4f" />

**Installed Programs – LaZagne Entry**<img width="1919" height="775" alt="lazagne-installed" src="https://github.com/user-attachments/assets/d6e1c3ef-3649-498e-b816-40c53d5f4ddd" />
 
**Network Monitoring Tool – LOOK@LAN**<img width="1919" height="743" alt="look@lan-installed" src="https://github.com/user-attachments/assets/ca0fa451-3f75-4745-b012-3c9303417aa8" />

**Image/Video Gallery View**<img width="1919" height="773" alt="media-gallery-preview" src="https://github.com/user-attachments/assets/6be80e0e-6082-48ff-a4fd-0955d6ec0d12" />

**Exploit Archive – Zerologon File**<img width="1919" height="775" alt="zerologon-exploit" src="https://github.com/user-attachments/assets/af273eba-669f-45fc-b3b2-1363a7dc0492" />

**YARA File Metadata / Author**<img width="1919" height="775" alt="yara-file-metadata" src="https://github.com/user-attachments/assets/cd585ec6-eb50-4a74-8baf-c86ed73aa1ec" />

**Keyword Search Results Example**<img width="1919" height="775" alt="keyword-search-hit" src="https://github.com/user-attachments/assets/0ccda078-3403-4ff9-bd23-932504f5cb5c" />

**Relevance to Career Goals:**
This room builds practical skills in forensic artifact analysis and reporting, which are directly applicable to roles in UK policing. STAR structured documents mirror court statements and professional forensic reports.

**Room Progress:** 100% completed, all 15 questions answered correctly.
