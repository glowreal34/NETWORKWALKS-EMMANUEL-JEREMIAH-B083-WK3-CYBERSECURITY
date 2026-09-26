<div align="center">

# 🔐 W3-PM2 - Password Cracking with NetworkWalks Tools

![Project](https://img.shields.io/badge/NetworkWalks-W3--PM2-red?style=for-the-badge)
![Hash Calculator](https://img.shields.io/badge/Tool-Hash%20Calculator-blue?style=for-the-badge)
![Password Cracker](https://img.shields.io/badge/Tool-Password%20Cracker-orange?style=for-the-badge)
![Dictionary Attack](https://img.shields.io/badge/Attack-Dictionary%20Attack-purple?style=for-the-badge)
![Windows](https://img.shields.io/badge/Platform-Windows%2010-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

**NetworkWalks Cybersecurity & Ethical Hacking Internship - Week 3**

</div>

---

## 👤 Project Information

| Field | Details |
|---|---|
| **Intern** | Emmanuel Jeremiah G. |
| **Batch** | B083-Networkwalks |
| **Week** | Week 3 |
| **Project Module** | W3-PM2 |
| **Project Title** | Password Cracking with NetworkWalks Tools |
| **Environment** | Windows 10 / Web Browser |
| **Status** | Completed |

---

## 📌 Project Overview

This project demonstrates the password-recovery process for a password-protected PDF using the browser-based security tools provided by NetworkWalks.

The practical exercise involved extracting the password hash from the protected PDF using the **NetworkWalks Hash Calculator**, transferring the complete `$pdf$` hash to the **NetworkWalks Password Cracker**, performing a dictionary-based password attack, recovering the correct password, and finally verifying the recovered credential by successfully opening the protected PDF.

Unlike W3-PM1, which used John the Ripper and the Johnny graphical interface, this module demonstrates a browser-based password-recovery workflow without requiring a locally installed password-cracking application.

---

## 🎯 Objective

The objective of this practical was to:

- Extract the password hash from a protected PDF file.
- Understand the role of a password hash during password recovery.
- Use the NetworkWalks Hash Calculator to obtain the PDF hash.
- Transfer the complete `$pdf$` hash into the NetworkWalks Password Cracker.
- Perform a dictionary-based password attack.
- Recover the correct password associated with the protected PDF.
- Verify the recovered password by successfully unlocking the file.
- Understand why weak or predictable passwords are vulnerable to password-cracking attacks.

---

## 🛠️ Tools and Resources

| Tool / Resource | Purpose |
|---|---|
| **Windows 10** | Host operating system used for the practical |
| **Google Chrome** | Web browser used to access the NetworkWalks tools and protected PDF |
| **NetworkWalks Hash Calculator** | Used to extract the password hash from the protected PDF |
| **NetworkWalks Password Cracker** | Used to perform the password-cracking attack against the extracted hash |
| **Protected PDF** | Authorized lab file provided for the password-recovery exercise |

---

## 🔄 Practical Workflow

```text
Protected PDF
      │
      ▼
NetworkWalks Hash Calculator
      │
      ▼
Extract $pdf$ Hash
      │
      ▼
Copy Complete Hash
      │
      ▼
NetworkWalks Password Cracker
      │
      ▼
Dictionary Attack
      │
      ▼
Password Recovered
      │
      ▼
Open Protected PDF
      │
      ▼
Verify Recovered Password
```

---

# 🧪 Practical Procedure

## 1. Preparing the Protected PDF

The password-protected PDF supplied for the practical exercise was downloaded and made available on the Windows system.

The working copy of the protected file appeared as:

`My-Locked-PDF1 (networkwalks).pdf`

The objective was to recover its password using the two browser-based NetworkWalks tools.

---

## 2. Opening the NetworkWalks Hash Calculator

The **NetworkWalks Hash Calculator** was opened in the web browser.

The Hash Calculator provides the first stage of the password-recovery workflow by processing the protected PDF and extracting the password-related hash information required for the cracking stage.

---

## 3. Uploading the Protected PDF and Extracting the Hash

The protected PDF was uploaded to the NetworkWalks Hash Calculator.

After processing the file, the tool identified the PDF as encrypted and produced a hash beginning with:

```text
$pdf$
```

The extracted hash represents the data that would subsequently be supplied to the password-cracking tool.

### 📸 Evidence - PDF Hash Extraction

<img width="1366" height="768" alt="W3-PM2-PDF-Hash-Extracted" src="https://github.com/user-attachments/assets/22b94224-8eb7-4b8e-9bd4-ca76ce6020a9" />

**Figure 1:** NetworkWalks Hash Calculator successfully processing the protected PDF and extracting the `$pdf$` hash required for password cracking.

---

## 4. Copying the Complete PDF Hash

The complete hash produced by the Hash Calculator was copied.

It was important to copy the **entire hash beginning with `$pdf$`** without removing or omitting any part of the value.

An incomplete or incorrectly copied hash could prevent the password-cracking tool from correctly processing the protected file.

---

## 5. Loading the Hash into the NetworkWalks Password Cracker

The **NetworkWalks Password Cracker** was opened in the browser.

The complete `$pdf$` hash obtained from the Hash Calculator was pasted into the password-cracking interface.

The interface showed a built-in password list containing **100 password candidates**, which would be tested against the supplied hash.

### 📸 Evidence - Hash Loaded into Password Cracker

<img width="1366" height="768" alt="W3-PM2-PDF-Hash-Loaded-in-Password-Cracker" src="https://github.com/user-attachments/assets/33302fed-6f7f-463b-bbb3-55414da64dcc" />

**Figure 2:** Extracted PDF hash loaded into the NetworkWalks Password Cracker and prepared for the dictionary attack.

---

## 6. Starting the Dictionary Attack

After the hash had been loaded correctly, the password-cracking process was started.

The tool performed a **dictionary attack**, testing candidate passwords from its available password list against the supplied PDF hash until a matching password was identified.

During the attack, the interface displayed the progress of the password attempts.

### 📸 Evidence - Password Cracking in Progress

<img width="1366" height="768" alt="W3-PM2-Password-Cracking-in-Progress" src="https://github.com/user-attachments/assets/91631983-d8a6-4784-9b7a-e7da785ad8dd" />

**Figure 3:** NetworkWalks Password Cracker actively testing password candidates. At the captured stage, the attack had processed 32 of the 100 available password candidates.

---

## 7. Recovering the Password

The dictionary attack continued until a matching password was found.

The successful match occurred at **91 out of 100 password attempts**, and the recovered password was:

```text
password1
```

The Password Cracker reported the successful match and displayed the recovered password.

### 📸 Evidence - Password Successfully Cracked

<img width="1366" height="768" alt="W3-PM2-Password-Successfully-Cracked" src="https://github.com/user-attachments/assets/2589c2b0-8b20-4e80-9886-4b5214a3d198" />

**Figure 4:** Successful dictionary attack showing the recovered password `password1` after a matching password candidate was identified.

---

## 8. Verifying the Recovered Password

Recovering a password from the cracking interface alone was not treated as the final verification.

The protected PDF was opened in the browser, which displayed a password prompt.

The recovered password:

```text
password1
```

was then entered into the protected PDF.

### 📸 Evidence - Protected PDF Password Prompt

<img width="1366" height="768" alt="W3-PM2-Protected-PDF-Password-Prompt" src="https://github.com/user-attachments/assets/c9e4c255-eb03-4302-a32e-1e5f484b24f3" />

**Figure 5:** Protected PDF requesting a password before access to its contents could be granted.

---

## 9. Successfully Unlocking the PDF

After the recovered password was submitted, the PDF opened successfully.

The displayed congratulatory page confirmed that the recovered password was valid and that the password-recovery process had been completed successfully.

### 📸 Evidence - PDF Successfully Unlocked

<img width="1366" height="768" alt="W3-PM2-PDF-Successfully-Unlocked" src="https://github.com/user-attachments/assets/7f93628e-0ab0-4d0a-8453-ffda88d006a5" />

**Figure 6:** Protected PDF successfully opened after authentication with the recovered password, confirming successful password recovery.

---

# 📊 Results

| Test / Activity | Result |
|---|---|
| Protected PDF processed | ✅ Successful |
| PDF hash extracted | ✅ Successful |
| Hash format identified | `$pdf$...` |
| Hash transferred to Password Cracker | ✅ Successful |
| Password attack initiated | ✅ Successful |
| Attack method | Dictionary-based password attack |
| Password candidates available | 100 |
| Successful match | 91 / 100 |
| Recovered password | `password1` |
| Recovered password verified | ✅ Successful |
| Protected PDF unlocked | ✅ Successful |
| Overall project status | **Completed Successfully** |

---

# 🔍 Technical Observations

## 1. Hash Extraction and Password Cracking Are Separate Stages

The practical demonstrated that extracting password-related hash information and recovering the actual password are two different operations.

The **Hash Calculator** first extracted the `$pdf$` hash from the protected file. The extracted hash was then supplied to the **Password Cracker**, which tested candidate passwords until a matching value was found.

This separation illustrates the basic workflow commonly encountered in password-recovery exercises:

```text
Protected Data → Hash Extraction → Candidate Testing → Password Recovery
```

---

## 2. The Complete Hash Must Be Preserved

The password-cracking stage depended on the complete `$pdf$` hash generated from the protected document.

Removing or omitting part of the extracted value could make the hash invalid for the cracking process. Therefore, preserving the complete hash during transfer between the two tools was an important part of the exercise.

---

## 3. The Practical Demonstrated a Dictionary-Based Attack

The Password Cracker used a predefined collection of password candidates and tested them sequentially against the supplied hash.

In this practical, the interface contained **100 candidate passwords**, and the correct password was identified at attempt **91/100**.

This demonstrates an important password-security principle: passwords that appear in an attacker's candidate list can be recovered without testing every theoretically possible character combination.

---

## 4. Browser-Based Tools Simplified the Workflow

Both NetworkWalks tools operated through the web browser.

This removed the need to install and configure a local password-cracking application for this module and provided a simplified workflow for understanding the relationship between:

- the protected file,
- the extracted hash,
- the password candidates,
- the matching process,
- and the recovered password.

---

## 5. Successful Cracking Should Be Verified

The recovered value was independently verified by using it to unlock the original protected PDF.

This verification step confirmed that `password1` was not merely displayed as a possible match by the cracking interface but was the valid password accepted by the protected document.

---

# 🧠 Key Learning Outcomes

Through this project, I gained practical understanding of:

- How a password-protected PDF can be prepared for password-recovery testing.
- The role of extracted password hashes in password-cracking workflows.
- How to extract a `$pdf$` hash from a protected PDF.
- Why the complete extracted hash must be preserved.
- How dictionary-based password cracking operates.
- How candidate passwords are tested until a valid match is identified.
- How browser-based security tools can be used to demonstrate password-recovery concepts.
- Why successful password recovery should be verified against the original protected resource.
- Why common and predictable passwords provide weaker resistance against dictionary attacks.

---

# 🛡️ Security Lessons

This practical reinforces the importance of strong password practices.

A password that exists in a cracking tool's dictionary or candidate list may be recovered relatively quickly when the corresponding protected data can be tested offline or through an authorized cracking environment.

Better password security therefore requires the use of passwords that are sufficiently long, difficult to predict, and resistant to common password-guessing strategies.

The exercise also demonstrates why organizations and users should avoid common passwords and predictable password patterns when protecting sensitive information.

---

# ⚖️ Ethical Use

Password cracking is a legitimate cybersecurity technique when performed within an authorized environment for purposes such as security assessment, password auditing, training, digital forensics, or controlled laboratory exercises.

This practical was performed exclusively against the **password-protected PDF provided for the NetworkWalks training exercise**.

Password-cracking techniques should only be used against systems, accounts, files, or data for which explicit authorization has been granted.

---

# ✅ Conclusion

W3-PM2 successfully demonstrated a complete browser-based password-recovery workflow using the **NetworkWalks Hash Calculator** and **NetworkWalks Password Cracker**.

The protected PDF was processed to obtain its `$pdf$` hash, the complete hash was transferred to the Password Cracker, and a dictionary attack was performed against the supplied hash.

The attack successfully recovered:

```text
password1
```

The recovered password was then verified by using it to unlock the protected PDF successfully.

Together with W3-PM1, this project provided practical exposure to two different password-recovery approaches: a locally configured John the Ripper/Johnny environment and a browser-based NetworkWalks toolset.

---

## 🔗 Navigation

⬅️ [W3-PM1 - Password Cracking with John the Ripper](W3-PM1-PASSWORD-CRACKING-WITH-JTR.md)

🏠 [Back to Week 3 README](README.md)

---

<div align="center">

**NetworkWalks Cybersecurity & Ethical Hacking Internship - Week 3**

**Emmanuel Jeremiah G. | B083-Networkwalks**

</div>
