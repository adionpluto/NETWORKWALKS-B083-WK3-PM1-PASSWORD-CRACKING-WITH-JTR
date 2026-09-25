# PASSWORD-RECOVERY-HASH-ANALYSIS-JTR-NETWORKWALKS

# Password Recovery & Hash Analysis — John the Ripper and NETWORKWALKS Tools

## Project Overview

This project documents the process of **auditing, extracting, and cracking password-protected PDF documents** using offline and web-based hash-cracking techniques.

The project uses the **John the Ripper (JTR) application** and **NETWORKWALKS Tools** to demonstrate how cryptographic hashes are generated from encrypted documents, extracted, and subjected to dictionary and brute-force attacks to recover credentials.

The project also demonstrates the verification of recovered passwords by successfully decrypting and accessing the original protected documents.

---

## Objectives

The project aims to:

* Understand how security handlers encrypt PDF files and how cryptographic signatures are represented in hash formats.
* Perform **offline hash cracking** using dictionary and brute-force attacks with the John the Ripper application.
* Perform **online password recovery** using NETWORKWALKS Tools.
* Verify recovered credentials by successfully decrypting and accessing protected PDF documents.
* Assess password strength and understand why short or predictable passwords can be vulnerable to hash-cracking utilities.

---

## Purpose of the Project

The project was undertaken to:

* Develop practical familiarity with **John the Ripper** and password-recovery workflows.
* Understand the process of extracting crackable hash information from encrypted PDF documents.
* Compare **offline and online password-cracking workflows**.
* Practice password recovery in a controlled and authorized environment.
* Understand the relationship between password complexity, entropy, and resistance to cracking attacks.
* Strengthen practical skills relevant to **Cybersecurity, Ethical Hacking, and Security Assessment**.

---

## Technologies Used

* **John the Ripper (JTR)** — Used for offline password recovery and hash cracking.
* **NETWORKWALKS Hash Calculator** — Used to extract PDF encryption hash signatures.
* **NETWORKWALKS Password Cracker** — Used for web-based password recovery.
* **Online PDF Hash Extractor** — Used to parse protected PDF files and export crackable hash strings.
* **Protected PDF Documents** — Used as the target files for authorized password-recovery testing.

---

## Introduction to Password Cracking

Password cracking is the process of recovering plain-text passwords from stored cryptographic hashes or encrypted containers.

Modern applications generally do not store passwords directly. Instead, they use mathematical hashes or encryption keys derived from passwords.

When attempting to access an encrypted document such as a protected PDF, the contents cannot be directly read without the appropriate credentials. The process therefore involves:

* Extracting the document's encryption parameters and hash structure.
* Passing the extracted hash to a cracking engine such as John the Ripper.
* Generating candidate passwords.
* Hashing the candidate passwords and comparing them against the target hash until a match is discovered.

---

## Technical Execution & Methodology

The password-recovery laboratory was completed using two approaches:

* **Method 1:** Offline attack using John the Ripper.
* **Method 2:** Web-based attack using NETWORKWALKS Tools.

### Method 1: Offline Attack via John the Ripper

#### Step 1: Hash Extraction via Online PDF Hash Converter

* Uploaded the target password-protected PDF file to an online hash-extraction utility.
* Converted the file information into a crackable hash string.
* Exported and saved the resulting hash output into a plain-text file.

![Hash Converter](./Screenshot%202026-09-23%20090219.png)

#### Step 2: Executing John the Ripper

* Launched the **John the Ripper (JTR) application**.
* Imported the saved hash file into the application interface.
* Selected the target wordlist dictionary.
* Initiated the cracking attack session.
* The JTR application processed candidate passwords until a matching password was identified.

![John the Ripper](./Screenshot%202026-09-23%20094223.png)

![Cracked Password](./Screenshot%202026-09-23%20094152.png)

#### Step 3: Verifying Document Access

* Copied the recovered plain-text password from the JTR application.
* Opened the original protected PDF file.
* Supplied the recovered password.
* Successfully unlocked and accessed the protected document.

![Successful PDF Access](./Screenshot%202026-09-23%20090848.png)

---

### Method 2: Web-Based Attack via NETWORKWALKS Tools

#### Step 1: Generating the Hash via Hash Calculator

* Navigated to the **NETWORKWALKS Hash Calculator** tool.
* Uploaded the target encrypted PDF file.
* Extracted its cryptographic hash signature.
* Received an extracted hash string beginning with the `$pdf$` format prefix.
* Copied the complete hash string to the clipboard.

![Hash Calculator](./Screenshot%202026-09-23%20093118.png)

#### Step 2: Cracking via NETWORKWALKS Password Cracker

* Opened a web browser and navigated to the **NETWORKWALKS Password Cracker** interface.
* Pasted the complete `$pdf$` hash string into the designated hash input field.
* Selected **Start Attack**.
* The tool initiated an automated process using candidate passwords until a match was identified.
* Received the interface message **"Password cracked successfully"** along with the recovered plain-text credential.

![Password Cracked](./Screenshot%202026-09-23%20091712.png)

#### Step 3: Document Decryption Verification

* Copied the recovered plain-text password from the NETWORKWALKS interface.
* Applied the recovered credential to the original PDF file.
* Successfully decrypted and accessed the protected document.

![PDF Decrypted Successfully](./Screenshot%202026-09-23%20093602.png)

---

# What I Learned

This project provided practical experience with password recovery, hash analysis, and encrypted-document security testing.

The main concepts covered were:

### 1. Hash Structure Standardization

I learned how PDF encryption signatures can be represented using structured formats containing identifiers such as `$pdf$`, which inform cracking engines about the underlying encryption scheme.

### 2. Offline vs. Online Cracking Workflows

I learned the difference between offline and online password-cracking workflows.

Offline cracking using dedicated applications such as **John the Ripper** allows local processing and the use of custom wordlists, while online utilities such as **NETWORKWALKS Tools** provide accessible web-based interfaces for hash matching.

### 3. Impact of Password Entropy

I observed how simple or dictionary-based passwords can be recovered quickly using password-cracking utilities.

This reinforced the importance of complex passphrases and strong organizational password policies.

### 4. Hash Formatting

I learned that preserving the complete structure of an extracted hash is important when transferring it between tools.

### 5. Wordlist Selection

I learned that the effectiveness of dictionary-based attacks depends partly on the coverage of the selected wordlist.

---

## Issues Faced During the Project

### 1. Hash Formatting Errors

Initially, copied hash strings omitted structural delimiters, preventing the John the Ripper application from properly parsing the hash.

Ensuring that the complete `$pdf$...` string was preserved resolved the issue.

### 2. Wordlist Coverage Limits

Default short wordlists failed to resolve the hash during early test iterations.

Loading a broader dictionary into the application resolved the password match.

---

## Security & Ethical Use

This project is intended exclusively for **educational activities, authorized security testing, and personal credential recovery**.

Password-recovery techniques should only be applied to files and systems for which explicit authorization has been obtained.

Unauthorized password attacks, access attempts, scanning, exploitation, or testing of systems and files are prohibited and violate cybersecurity ethics.

---

## Tools & Resources

* **John the Ripper (JTR):** Offline GUI application for password recovery and hash cracking.
* **Online PDF Hash Extractor:** Web utility used to parse protected PDF files and export crackable hash strings.
* **NETWORKWALKS Hash Calculator:** Online tool for extracting PDF signature hashes beginning with `$pdf$`.
* **NETWORKWALKS Password Cracker:** Web-based interface for password-recovery attacks.

---

# Author

*Aditya Choubey*  
**Computer Science Student**

[LinkedIn](https://www.linkedin.com/in/adityachby/) 

---

## Project Information

**Program Name:** Cybersecurity at Networkwalks | **Week:** 03 | **Project:** PASSWORD RECOVERY HASH ANALYSIS JTR | **Repository:** GitHub
