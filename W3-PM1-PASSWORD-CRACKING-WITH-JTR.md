<div align="center">

# 🔐 W3-PM1: Password Cracking with John the Ripper

![Project](https://img.shields.io/badge/NetworkWalks-W3--PM1-red?style=for-the-badge)
![John the Ripper](https://img.shields.io/badge/Tool-John%20the%20Ripper-black?style=for-the-badge)
![Johnny](https://img.shields.io/badge/GUI-Johnny-orange?style=for-the-badge)
![Password Security](https://img.shields.io/badge/Focus-Password%20Security-purple?style=for-the-badge&logo=keycdn&logoColor=white)
![Windows](https://img.shields.io/badge/Platform-Windows%2010-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

**NetworkWalks Cybersecurity & Ethical Hacking Internship**  
**Intern:** Emmanuel Jeremiah G.  
**Batch:** B083-Networkwalks  
**Week:** 3  
**Project Module:** W3-PM1

</div>

---

## 📌 Project Overview

This project documents the completion of **Week 3 — Project Module 1 (W3-PM1)** of the NetworkWalks Cybersecurity & Ethical Hacking Internship.

The practical focused on **password recovery from a password-protected PDF file using John the Ripper (JTR) and Johnny on Windows**.

John the Ripper is a password-cracking tool capable of testing password hashes and password-protected files. Johnny provides a graphical user interface for John the Ripper, allowing its password-cracking functionality to be operated through a GUI.

During the lab, a crackable hash was extracted from the provided password-protected PDF and prepared for processing by John the Ripper. Johnny was configured to use the John executable, the extracted hash was loaded, and a password-cracking attack was executed.

The attack successfully recovered the password:

```text
good-luck
```

The recovered password was subsequently verified by using it to unlock the protected PDF successfully.

The practical also produced an important troubleshooting experience involving the location of `john.exe` and its runtime dependencies.

---

## 🎯 Project Objective

The objective of this practical was to:

> Recover the password of the provided `My Locked PDF1.pdf` file using John the Ripper and Johnny on a Windows system.

The exercise also provided practical exposure to:

- Password-protected PDF files
- PDF hash extraction
- Password hashes
- John the Ripper
- Johnny GUI
- Password cracking
- Password recovery
- Application dependencies
- Troubleshooting
- Password verification

---

## 🛠️ Tools & Resources Used

| Tool / Resource | Purpose |
|---|---|
| **Windows 10** | Host operating system used for the practical |
| **John the Ripper (JTR)** | Password-cracking engine |
| **Johnny** | Graphical user interface for John the Ripper |
| **OnlineHashCrack PDF Hash Extractor** | Used to extract the crackable `$pdf$` hash from the protected PDF |
| **Google Chrome** | Used to access the online PDF hash extraction service and open the protected PDF |
| **Notepad / Text File** | Used to save the extracted PDF hash as `hash1.txt` |
| **My Locked PDF1.pdf** | Password-protected laboratory file used for the exercise |

---

## 🔄 Practical Workflow

The practical followed this general workflow:

```text
My Locked PDF1.pdf
        │
        ▼
Extract PDF Hash
        │
        ▼
Copy Complete $pdf$ Hash
        │
        ▼
Save Hash as hash1.txt
        │
        ▼
Configure Johnny with John the Ripper
        │
        ▼
Load hash1.txt
        │
        ▼
Start Password Attack
        │
        ▼
Recover Password
        │
        ▼
Verify Password Against Protected PDF
        │
        ▼
Successfully Unlock PDF
```

---

# 🧪 Practical Procedure

## 1. Preparing John the Ripper

John the Ripper was obtained for the Windows environment as required for the practical.

The package contains the John password-cracking engine together with the supporting files and runtime dependencies required for its operation.

Rather than treating `john.exe` as an independent executable, the complete John the Ripper package must remain properly extracted so that John can access the supporting components it requires.

This became particularly important during the troubleshooting stage of the project.

---

## 2. Installing and Opening Johnny

Johnny was installed and opened on the Windows system.

Johnny acts as the graphical interface through which John the Ripper can be configured and operated. This allows password files to be loaded and attacks to be initiated through a graphical environment.

The next requirement was to configure Johnny with the correct location of the John the Ripper executable.

---

## 3. Extracting the Hash from the Protected PDF

The provided laboratory file:

```text
My Locked PDF1.pdf
```

was password protected.

To perform password recovery with John the Ripper, a crackable hash first had to be extracted from the protected PDF.

The PDF was uploaded to the OnlineHashCrack PDF Hash Extractor. The service processed the file and produced a hash beginning with:

```text
$pdf$
```

The complete hash was then copied for use in the password-cracking process.

### 📸 Evidence: PDF Hash Extraction

<img width="1366" height="768" alt="W3-PM1-PDF-Hash-Extraction" src="https://github.com/user-attachments/assets/2e34fa48-8ad4-4e52-9afb-d9bbf5c07440" />

*Figure 1: Crackable `$pdf$` hash successfully extracted from `My Locked PDF1.pdf`.*

The screenshot confirms that the protected PDF was processed successfully and that a PDF hash suitable for password-cracking tools was generated.

---

## 4. Preparing the Hash File

The complete extracted hash was copied into a text file.

The hash was saved as:

```text
hash1.txt
```

The hash value was preserved in the required `$pdf$...` format so that John the Ripper could correctly recognize and process it.

This text file served as the password/hash input subsequently loaded into Johnny.

---

## 5. Configuring Johnny with John the Ripper

Johnny requires the location of the John the Ripper executable before it can launch the cracking engine.

The correct `john.exe` was selected from the `run` directory of the properly extracted John the Ripper package.

The executable remained inside its original extracted environment together with its required supporting files.

### 📸 Evidence: Correct John Executable Configuration

<img width="1366" height="768" alt="W3-PM1-Johnny-John-Executable-Configuration" src="https://github.com/user-attachments/assets/baf35c64-cae6-4bcf-937a-21a22e267b17" />

*Figure 2: The correct `john.exe` identified inside the extracted John the Ripper `run` directory.*

This configuration became particularly significant because an earlier attempt to use a relocated copy of `john.exe` resulted in an execution failure.

---

# ⚠️ Challenge Encountered: John Execution Failure

During the initial configuration, I moved `john.exe` from its original extracted John the Ripper directory into another folder.

The assumption was that the executable could be moved and operated independently.

Johnny was then configured to use the relocated executable.

When the password attack was started, Johnny returned the following error:

```text
John crashed. Verify the Console Log for details.
```

### 📸 Evidence: Johnny Reporting John Crash

<img width="511" height="133" alt="W3-PM1-John-Missing-DLL-Error" src="https://github.com/user-attachments/assets/b9713bdb-6374-4a96-b06c-2b9084d7a8bf" />

*Figure 3: Johnny reporting that the configured John executable crashed during execution.*

The failure prompted further troubleshooting rather than repeatedly restarting the same attack.

---

## 🔎 Troubleshooting and Root-Cause Analysis

The configured `john.exe` was tested directly outside Johnny to determine whether the failure originated from Johnny or from John itself.

Direct execution revealed that John could not start because a required runtime dependency, `cygcrypt-2.dll`, could not be located.

This established that the problem was not caused by:

- The extracted PDF hash
- `hash1.txt`
- The password attack itself
- Johnny's attack interface

Instead, the issue resulted from moving `john.exe` away from the directory containing the supporting files and libraries required for its execution.

This demonstrated an important application-dependency concept:

> An executable file is not necessarily a self-contained application. It may depend on DLLs, configuration files, libraries, and other resources located within its original application directory.

---

## 🛠️ Resolution

To resolve the problem:

1. The independently relocated copy of `john.exe` was deleted.
2. I returned to the original John the Ripper archive.
3. The complete archive was extracted properly.
4. The original directory structure and supporting files were kept together.
5. Johnny was configured again.
6. The `john.exe` located within the extracted John the Ripper `run` directory was selected.
7. The password attack was restarted.

After correcting the executable location and preserving its required dependencies, John executed successfully through Johnny.

The attack was able to run to completion.

The successful configuration is shown in **Figure 2**, where `john.exe` is located inside the properly extracted John the Ripper `run` directory.

---

## 6. Loading the Extracted Hash into Johnny

After John the Ripper was correctly configured, the previously prepared:

```text
hash1.txt
```

file was opened in Johnny using the password-file option.

Johnny recognized the PDF hash and prepared it for processing by the John the Ripper engine.

No separate screenshot was captured for this intermediate step; however, the successful recognition and cracking of the PDF hash in the subsequent result confirms that the hash file was loaded and processed correctly.

---

## 7. Starting the Password Attack

With the PDF hash loaded into Johnny and the correct John executable configured, a new password attack was started.

Johnny invoked John the Ripper to process the supplied PDF hash and test candidate passwords.

After the executable-location issue had been resolved, the attack ran successfully to completion.

---

## 8. Successful Password Recovery

John the Ripper successfully identified the password associated with the protected PDF hash.

The recovered password was:

```text
good-luck
```

Johnny displayed the recovered password together with the PDF hash and showed the attack as completed.

### 📸 Evidence: Password Successfully Recovered

<img width="888" height="693" alt="W3-PM1-Password-Recovered-with-Johnny" src="https://github.com/user-attachments/assets/9b9f7673-6b6f-4f36-996f-f388d341df65" />

*Figure 4: Johnny displaying the successfully recovered password `good-luck` for the PDF hash.*

This confirmed that the password-cracking phase of the practical had completed successfully.

---

# 🔓 Password Verification

Recovering a candidate password alone does not fully validate a password-cracking result.

The recovered value must be tested against the original protected resource to confirm that it is actually correct.

## 9. Opening the Protected PDF

The original:

```text
My Locked PDF1.pdf
```

file was opened again.

The browser's PDF viewer detected the document protection and displayed a password prompt.

### 📸 Evidence: Protected PDF Requesting Password

<img width="1366" height="768" alt="W3-PM1-Protected-PDF-Password-Prompt" src="https://github.com/user-attachments/assets/f2f361b9-f844-43a8-be50-00069910ce5e" />

*Figure 5: `My Locked PDF1.pdf` requesting a password before access to its contents was permitted.*

The recovered password:

```text
good-luck
```

was entered into the password field and submitted.

---

## 10. Successful PDF Unlock

The password was accepted successfully.

The protected document opened and displayed its NetworkWalks congratulatory page and captured flag, confirming successful access to the protected content.

### 📸 Evidence — PDF Successfully Unlocked

<img width="1366" height="768" alt="W3-PM1-PDF-Successfully-Unlocked" src="https://github.com/user-attachments/assets/98e73aed-56ec-4fb1-b575-8ce7106db063" />

*Figure 6: Protected PDF successfully opened after verification of the recovered password.*

This provided final verification that:

```text
good-luck
```

was the correct password for the protected PDF used during W3-PM1.

---

# 📊 Results

| Item | Result |
|---|---|
| Protected file | `My Locked PDF1.pdf` |
| Hash type | PDF hash (`$pdf$...`) |
| Password-cracking engine | John the Ripper |
| Graphical interface | Johnny |
| Hash input file | `hash1.txt` |
| Attack execution | Successful |
| Recovered password | `good-luck` |
| Password verification | Successful |
| Protected PDF unlocked | Yes |
| Project status | ✅ Completed |

---

# 🔍 Technical Observations

## 1. Password Cracking Did Not Reveal the Password Directly from the Hash

The extracted `$pdf$` value was not simply converted back into plaintext.

Instead, John the Ripper tested password candidates and evaluated them against the protected PDF hash until a valid match was identified.

This distinction is important because hashing is designed as a one-way process rather than a directly reversible transformation.

---

## 2. Hash Extraction and Password Cracking Were Separate Stages

The practical demonstrated two distinct operations:

```text
Protected PDF → Hash Extraction
```

followed by:

```text
Extracted Hash → Password Cracking
```

The hash extractor prepared the protected file information in a format that the password-cracking engine could process.

John the Ripper then performed the password-recovery operation.

---

## 3. Tool Configuration Directly Affected Attack Execution

Johnny itself was operational during the initial failed attempt, but it could not successfully use the relocated John executable.

This demonstrated that a graphical frontend can depend on an underlying command-line engine being correctly installed and configured.

In this practical:

```text
Johnny
   ↓
Invokes
   ↓
John the Ripper
   ↓
Processes PDF Hash
   ↓
Returns Password Result
```

Therefore, a failure in the underlying John executable prevented Johnny from completing the attack.

---

## 4. Executable Files May Depend on Their Runtime Environment

The troubleshooting process demonstrated that copying or moving an `.exe` file does not guarantee that the application will continue to operate.

John depended on supporting components within its extracted environment.

Separating the executable from those components resulted in the observed execution failure.

---

## 5. Verification Is an Essential Final Step

A cracking tool reporting a password is strong evidence of successful recovery, but validating the password against the protected file provides direct confirmation.

The final PDF-unlock stage therefore served as verification of the password-recovery result.

---

# 🧠 Key Learning Outcomes

Through this project, I gained practical experience in:

- Understanding the relationship between password-protected files and crackable hashes.
- Extracting a PDF hash for password-recovery purposes.
- Preparing an extracted hash in a text file for processing.
- Configuring Johnny to use John the Ripper.
- Loading a password/hash file into Johnny.
- Executing a password-cracking attack.
- Recovering a password from a protected PDF.
- Verifying a recovered password against the original file.
- Diagnosing an application execution failure.
- Understanding the importance of runtime dependencies.
- Distinguishing a frontend application from its underlying cracking engine.
- Documenting troubleshooting as part of a cybersecurity workflow.

---

# 🔐 Security Lessons

The practical demonstrated why predictable passwords can present a significant security risk.

Password-cracking tools can systematically test candidate passwords against protected data. If the correct password exists within the candidates being tested, the password may be recovered.

This reinforces the importance of using passwords that are:

- Sufficiently long
- Difficult to predict
- Unique
- Not based on common words or simple patterns
- Resistant to common dictionary-based password attacks

The project also demonstrated that password security depends not only on the encryption or protection mechanism but also on the strength of the password protecting the resource.

---

# ⚖️ Ethical Use Statement

This password-cracking exercise was performed exclusively within an **authorized NetworkWalks cybersecurity training laboratory**.

The password-protected PDF used in this project was provided specifically for the practical exercise.

The techniques documented here are intended for:

- Cybersecurity education
- Authorized penetration testing
- Password-security auditing
- Ethical hacking laboratories
- Defensive security research

Password-cracking techniques should only be used against files, systems, accounts, or other resources for which explicit authorization has been granted.

---

# 🏁 Conclusion

W3-PM1 successfully demonstrated the practical process of recovering a password from a protected PDF using **John the Ripper and Johnny**.

The project involved extracting the PDF hash, preparing it as `hash1.txt`, configuring Johnny with the John the Ripper executable, executing the password attack, recovering the password `good-luck`, and verifying the result by successfully unlocking the original protected PDF.

The project also provided a valuable troubleshooting experience.

Moving `john.exe` away from the rest of the extracted John the Ripper environment caused the executable to fail because a required runtime dependency could no longer be located. Identifying the root cause and restoring the complete extracted directory allowed the attack to execute successfully.

This reinforced an important practical cybersecurity principle:

> Successful security testing requires more than knowing which tool to use; it also requires understanding how the tool operates, recognizing failures, identifying their causes, and applying technically correct solutions.

**W3-PM1 Status: ✅ Successfully Completed**

---

## ⬅️ Navigation

[⬅️ Back to Week 3 README](README.md) | [W3-PM2 — Password Cracking with NetworkWalks Tools ➡️](W3-PM2-PASSWORD-CRACKING-WITH-NETWORKWALKS-TOOLS.md)

---

<div align="center">

**Emmanuel Jeremiah G.**  
**B083-Networkwalks**

*NetworkWalks Cybersecurity & Ethical Hacking Internship — Week 3*

</div>
