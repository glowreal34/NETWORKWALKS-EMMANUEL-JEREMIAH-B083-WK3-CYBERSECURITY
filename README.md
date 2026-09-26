<div align="center">

# 🔐 NetworkWalks Cybersecurity Internship: Week 3

## Password Cracking & Password Security

![Cybersecurity](https://img.shields.io/badge/Skill-Cybersecurity-blue?style=for-the-badge&logo=hackthebox&logoColor=white)
![Week 3](https://img.shields.io/badge/NetworkWalks-Week%203-red?style=for-the-badge)
![Password Security](https://img.shields.io/badge/Focus-Password%20Security-purple?style=for-the-badge&logo=keycdn&logoColor=white)
![John the Ripper](https://img.shields.io/badge/Tool-John%20the%20Ripper-black?style=for-the-badge)
![Johnny](https://img.shields.io/badge/Tool-Johnny-orange?style=for-the-badge)
![Windows](https://img.shields.io/badge/Platform-Windows%2010-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

**Intern:** Emmanuel Jeremiah G.  
**Batch:** B083-Networkwalks  
**Program:** Cybersecurity & Ethical Hacking Internship  
**Week:** 3

</div>

---

## 📌 Project Overview

This repository documents my **Week 3 practical projects** completed during the NetworkWalks Cybersecurity & Ethical Hacking Internship.

The week's practical work focused on **password cracking and password security**, particularly the process of recovering passwords from password-protected PDF files.

Two project modules were completed using different approaches:

- **W3-PM1: Password Cracking with John the Ripper (JTR)**
- **W3-PM2: Password Cracking with NetworkWalks Tools**

The first module involved using **John the Ripper and Johnny** to process and crack a password-protected PDF hash. The second module demonstrated a browser-based approach using the **NetworkWalks Hash Calculator and Password Cracker**.

Together, the projects provided practical exposure to password-protected files, PDF hash extraction, dictionary-based password cracking, password recovery, troubleshooting, and verification of recovered credentials.

---

## 🎯 Project Objectives

The objectives of the Week 3 practical exercises were to:

- Understand the basic principles of password cracking and password recovery.
- Understand the role of hashes in password-protected files.
- Extract a crackable hash from a password-protected PDF.
- Use **John the Ripper (JTR)** as a password-cracking engine.
- Use **Johnny** as a graphical interface for John the Ripper.
- Use the **NetworkWalks Hash Calculator** to extract a PDF hash.
- Use the **NetworkWalks Password Cracker** to perform a dictionary-based password attack.
- Recover passwords from the provided laboratory PDF files.
- Verify recovered passwords by successfully opening the protected files.
- Develop practical troubleshooting skills when security tools fail to execute correctly.
- Understand why weak and predictable passwords present a security risk.

---

## 🧪 Week 3 Project Modules

### 🔹 W3-PM1: Password Cracking with John the Ripper

This module focused on recovering the password of a protected PDF using **John the Ripper (JTR)** together with its graphical interface, **Johnny**, on Windows.

The practical involved extracting the PDF hash, preparing the extracted hash for processing, configuring Johnny to use the correct John the Ripper executable, executing the password-cracking attack, recovering the password, and validating the result against the protected PDF.

A significant troubleshooting scenario was also encountered during this module when the John executable failed after being moved away from its original extracted directory. The issue was investigated and resolved by restoring the proper John the Ripper directory structure and using the executable together with its required dependencies.

**Recovered Password:** `good-luck`

**Status:** ✅ Successfully Completed

➡️ **[View the complete W3-PM1 technical documentation](W3-PM1-PASSWORD-CRACKING-WITH-JTR.md)**

---

### 🔹 W3-PM2: Password Cracking with NetworkWalks Tools

This module explored password recovery through the browser-based security tools provided by NetworkWalks.

The protected PDF was processed using the **NetworkWalks Hash Calculator**, which extracted a crackable `$pdf$` hash. The extracted hash was then submitted to the **NetworkWalks Password Cracker**, where a dictionary-based attack tested password candidates until the correct password was identified.

The recovered password was subsequently verified by using it to unlock the protected PDF successfully.

**Recovered Password:** `password1`

**Status:** ✅ Successfully Completed

➡️ **[View the complete W3-PM2 technical documentation](W3-PM2-PASSWORD-CRACKING-WITH-NETWORKWALKS-TOOLS.md)**

---

## 🛠️ Tools & Technologies Used

| Tool / Technology | Purpose |
|---|---|
| **Windows 10** | Host operating system used for the practical exercises |
| **John the Ripper (JTR)** | Password-cracking engine used in W3-PM1 |
| **Johnny** | Graphical user interface used to operate John the Ripper |
| **OnlineHashCrack PDF Hash Extractor** | Used during W3-PM1 to extract the crackable hash from the protected PDF |
| **NetworkWalks Hash Calculator** | Used during W3-PM2 to extract the protected PDF hash |
| **NetworkWalks Password Cracker** | Used to perform the browser-based dictionary attack in W3-PM2 |
| **Google Chrome** | Web browser used to access the browser-based tools and verify the protected PDFs |
| **Password-Protected PDF Files** | Authorized laboratory targets used for password-recovery exercises |

---

## ⚙️ Practical Workflow

The Week 3 exercises demonstrated the general password-recovery workflow:

```text
Password-Protected PDF
        │
        ▼
Extract Crackable PDF Hash
        │
        ▼
Load Hash into Password-Cracking Tool
        │
        ▼
Perform Password Attack
        │
        ▼
Identify Matching Password
        │
        ▼
Verify Recovered Password
        │
        ▼
Successfully Unlock Protected PDF
```

Although both project modules followed this general concept, they implemented it through different toolsets.

**W3-PM1**

```text
Protected PDF
     ↓
PDF Hash Extraction
     ↓
Hash File
     ↓
Johnny + John the Ripper
     ↓
Password Recovery
     ↓
PDF Verification
```

**W3-PM2**

```text
Protected PDF
     ↓
NetworkWalks Hash Calculator
     ↓
$pdf$ Hash
     ↓
NetworkWalks Password Cracker
     ↓
Dictionary Attack
     ↓
Password Recovery
     ↓
PDF Verification
```

---

## 📊 Project Results

| Project Module | Approach | Result | Status |
|---|---|---|---|
| **W3-PM1** | John the Ripper + Johnny | Password recovered and protected PDF successfully unlocked | ✅ Completed |
| **W3-PM2** | NetworkWalks Hash Calculator + Password Cracker | Password recovered and protected PDF successfully unlocked | ✅ Completed |

Both password-recovery approaches successfully achieved their respective laboratory objectives.

---

## 🔧 Troubleshooting Experience

W3-PM1 provided an additional practical troubleshooting experience beyond the normal password-cracking workflow.

During the initial configuration, `john.exe` had been moved from the extracted John the Ripper directory into another folder under the assumption that the executable could operate independently.

When Johnny attempted to invoke this relocated executable, **John failed to execute correctly**. Further investigation showed that the executable depended on supporting files and libraries located within the original John the Ripper directory structure.

The issue was resolved by:

1. Removing the independently relocated copy of `john.exe`.
2. Returning to the original John the Ripper archive.
3. Extracting the complete package correctly.
4. Preserving the original directory structure and dependencies.
5. Configuring Johnny to use `john.exe` from the properly extracted John the Ripper directory.
6. Re-running the attack successfully.

This troubleshooting process reinforced an important technical lesson: **an executable file is not necessarily a standalone application**. Applications may rely on dynamic-link libraries, configuration files, and other runtime dependencies located within their installation or extracted directories.

The complete troubleshooting process and supporting evidence are documented in the **W3-PM1 technical documentation**.

---

## 🧠 Key Learning Outcomes

Completing the Week 3 practicals strengthened my understanding of several important cybersecurity concepts.

### Password Cracking

Password cracking involves attempting to recover a password by testing candidate values against password-related data until a valid match is identified.

### Hash-Based Password Recovery

Rather than directly reading the original password from a protected file, password-cracking tools can work with an extracted hash representation and test candidate passwords against it.

### Dictionary Attacks

A dictionary attack tests passwords from a predefined wordlist or collection of likely password candidates. Passwords that are common, predictable, or included in such lists are therefore significantly more vulnerable to this type of attack.

### Tool Dependencies

Security tools may depend on supporting libraries and files. Moving only an executable away from its required runtime dependencies can prevent the application from functioning correctly.

### Troubleshooting

Error messages should be investigated rather than treated only as failures. The John the Ripper execution problem demonstrated how identifying the actual cause of an error can lead to a reliable technical solution.

### Verification

Recovering a candidate password is not the final stage of the process. The password must be validated against the protected resource to confirm that the recovery was successful.

---

## 🔐 Security Takeaway

The exercises demonstrated why password strength remains an important security control.

Passwords that are common or predictable can be vulnerable to dictionary-based attacks because an attacker or security-testing tool may only need to test a relatively small collection of likely passwords before finding a match.

More resilient passwords should therefore avoid common words and predictable patterns and should use sufficient length and unpredictability.

Password cracking can be valuable in legitimate security assessments, password audits, digital forensics, controlled laboratory exercises, and authorized penetration testing. However, the same techniques can be abused when performed without authorization.

---

## ⚖️ Ethical Use Statement

All password-cracking activities documented in this repository were performed **strictly within an authorized cybersecurity training environment** as part of the NetworkWalks Cybersecurity & Ethical Hacking Internship.

The password-protected files used during these exercises were provided specifically for laboratory practice.

The techniques and tools documented in this repository are presented for:

- Cybersecurity education
- Authorized security testing
- Password-security assessment
- Ethical hacking laboratories
- Defensive security research

They should only be used against systems, accounts, files, or resources for which explicit authorization has been granted.

---

## 📂 Repository Structure

| File / Directory | Description |
|---|---|
| `README.md` | Main Week 3 project overview and navigation |
| `W3-PM1-PASSWORD-CRACKING-WITH-JTR.md` | Complete documentation for Project Module 1 — Password Cracking with John the Ripper and Johnny |
| `W3-PM2-PASSWORD-CRACKING-WITH-NETWORKWALKS-TOOLS.md` | Complete documentation for Project Module 2 — Password Cracking with NetworkWalks Tools |
| `screenshots/` | Contains all screenshot evidence captured during W3-PM1 and W3-PM2 |

---

## 📚 Project Documentation

Detailed procedures, screenshots, observations, results, troubleshooting, and technical explanations are available in the individual project-module documentation:

### 📄 Project Module 1

**[W3-PM1: Password Cracking with John the Ripper](W3-PM1-PASSWORD-CRACKING-WITH-JTR.md)**

Covers:

- John the Ripper and Johnny setup
- PDF hash extraction
- Hash preparation
- Johnny configuration
- Password-cracking process
- John execution failure
- Troubleshooting and resolution
- Successful password recovery
- PDF verification
- Technical observations and lessons learned

### 📄 Project Module 2

**[W3-PM2: Password Cracking with NetworkWalks Tools](W3-PM2-PASSWORD-CRACKING-WITH-NETWORKWALKS-TOOLS.md)**

Covers:

- NetworkWalks Hash Calculator
- PDF hash extraction
- Hash transfer to the Password Cracker
- Dictionary-based password attack
- Successful password recovery
- PDF verification
- Technical observations and lessons learned

---

## 🏁 Conclusion

Week 3 provided practical experience with two approaches to password recovery.

W3-PM1 demonstrated password cracking using **John the Ripper and Johnny**, while W3-PM2 demonstrated the same underlying security concept through the browser-based **NetworkWalks Hash Calculator and Password Cracker**.

Beyond successfully recovering the laboratory passwords, the exercises strengthened my understanding of PDF hash extraction, dictionary-based password attacks, password strength, tool dependencies, troubleshooting, and the importance of validating security-testing results.

The troubleshooting encountered during W3-PM1 was particularly valuable because it demonstrated that practical cybersecurity work involves not only operating tools but also understanding their dependencies, diagnosing failures, and restoring a functional testing environment.

---

## 🙏 Acknowledgement

Special appreciation to **NetworkWalks** and the instructors for providing the practical laboratory exercises, tools, guidance, and structured learning environment used throughout this week's cybersecurity training.

The Week 3 projects provided an opportunity to move beyond theoretical password-security concepts and apply them through practical, controlled, and authorized exercises.

---

<div align="center">

### 🔐 Cybersecurity is learned by understanding, testing, troubleshooting, and documenting.

**Emmanuel Jeremiah G.**  
*B083-Networkwalks*

</div>
