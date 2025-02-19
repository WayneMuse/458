# Malware Analysis - CPSC 458

## Project Overview

This repository contains detailed analyses of multiple malware samples as part of **CPSC 458-03 Fall 2024: Malware Analysis**. Each project follows a structured methodology, utilizing static analysis, dynamic analysis, reverse engineering, and behavior monitoring to dissect and understand malware behavior. The projects focus on unpacking, debugging, and analyzing malicious executables to identify Indicators of Compromise, persistence mechanisms, and network activity.

##**Projects & Exercises**

### **1. Projects**
- **Project 1: PE32+ Executable Analysis**
  - Used **Remnux, Die, PEStudio, and ProcMon** for static and dynamic analysis.
  - Identified Windows API calls for **network communication, registry modifications, and user information retrieval**.
  - Analyzed function imports like `WS2_32.dll` (networking), `SHELL32.dll` (shell execution), and `ADVAPI32.dll` (registry manipulation).
- **Project 2: Suspicious PowerShell Utility**
  - Investigated a fake PowerShell script designed to **exfiltrate system memory data**.
  - Used **Process Explorer, ProcMon, and Wireshark** to detect hidden registry and network activity.
  - Identified **C2 communication patterns** and mitigated the malware via VM snapshots.
- **Project 3: Hash Utility with Hidden Network Features**
  - Reverse-engineered **HashUtil.exe**, which disguised itself as a hashing tool but connected to a **C2 server**.
  - Used **Ghidra, x64dbg, and PEStudio** to reveal **self-modifying behavior and anti-debugging techniques**.
  - Observed **packet captures and DNS requests to malicious domains**.
- **Project 4: Nim-based Malware & Evasion Techniques**
  - Analyzed **Depends22_x64**, which masqueraded as a legitimate program.
  - Used **Detect-It-Easy (DIE), Process Monitor, and Dependency Walker** to uncover **network manipulation, process injection, and keylogging**.
  - Discovered **anti-analysis techniques using the Nim programming language** to obfuscate malicious behavior.

### **2. Labs**
- **Exercise 1: Identifying Malware Indicators**
  - Extracted **host-based and network-based IoCs** from a malware sample.
  - Simulated malicious network traffic with **ApateDNS and Wireshark**.
- **Exercise 2: Decompiling & Analyzing Blaster Worm**
  - Used **Ghidra** to **decompile and rename functions** for clearer analysis.
  - Identified **Blaster_DoS_thread() and Blaster_Spreader()** used for network propagation.
- **Exercise 3: Unpacking & Debugging**
  - Unpacked a **packed malware sample** using **x64dbg and Scylla**.
  - Debugged and dumped the unpacked binary for further analysis in **Ghidra**.
- **Exercise 4: YARA Rule Creation**
  - Developed **custom YARA rules** to detect malware families based on **Project 1 and Project 3 samples**.
  - Verified **malware signatures without false positives**.

## **Tools Used**
- **Static Analysis**: PEStudio, Detect-It-Easy (DIE), Ghidra, YARA
- **Dynamic Analysis**: ProcMon, Process Explorer, x64dbg, ApateDNS, Wireshark
- **Reverse Engineering**: Ghidra, Scylla, x64dbg
- **Malware Testing Environment**: Windows 10 VM, Remnux
