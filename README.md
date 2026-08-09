# RoguePlanet - Interactive Post-Exploitation Menu

## Overview
This version of RoguePlanet includes an **interactive menu system** with 15 post-exploitation options that execute automatically after gaining SYSTEM privileges through the Windows Defender vulnerability.

Upon successful exploitation, instead of just spawning a basic shell, the program presents a professional menu with pre-built actions for further system compromise.

## Menu Options

### **[0] Launch CMD**
Opens an interactive Command Prompt with SYSTEM privileges. Execute any commands needed for further exploitation or reconnaissance.

### **[1] System Information**
Displays comprehensive system details:
- OS version and build number
- Processor info
- RAM and disk space
- Network configuration (IP, DNS, DHCP)
- Running processes and services
- Logged-in users and credentials info
- Installed Windows updates
- Drive information

### **[2] List Users**
Enumerates all local user accounts with details:
- Local users and administrators
- Group memberships
- User SIDs and descriptions
- Account status and security info

### **[3] Protected Files**
Accesses sensitive system files that are normally protected:
- SAM, SECURITY, SYSTEM registry hives
- Windows hosts file
- System32 directory listing

### **[4] Export Credential Hashes**
Extracts and displays NTLM password hashes:
- Copies SAM/SYSTEM/SECURITY files to %TEMP%
- Shows hash format for offline cracking
- References popular cracking tools (Hashcat, John the Ripper)

### **[5] Create Hidden Admin**
Creates a backdoor administrative account:
- Username: "backdoor"
- Password: "P@ssw0rd123!"
- Hidden from Settings and User Management
- Persistent across reboots

### **[6] Disable Windows Defender**
Disables Windows Defender protections:
- Disables real-time monitoring
- Disables automatic updates
- Disables cloud-based protection
- Stops WinDefend service

### **[7] Install Backdoor**
Creates a persistent backdoor via Scheduled Task:
- Task name: "Windows Update Service"
- Executes on system startup
- Runs with SYSTEM privileges
- Survives system reboots

### **[8] Enable RDP**
Enables Remote Desktop Protocol for remote access:
- Activates RDP service
- Opens Windows Firewall for RDP (port 3389)
- Adds backdoor user to RDP group
- Allows remote administration

### **[9] Browser History**
Extracts browser history locations from:
- Google Chrome/Chromium
- Microsoft Edge
- Mozilla Firefox
- Displays paths to SQLite databases

### **[10] Access Other Users**
Lists accessible directories of other user accounts:
- Documents, Downloads, Desktop folders
- Sensitive user data locations
- Shared folders and network paths

### **[11] LSASS Dump**
Explains LSASS memory dumping technique:
- Extract plaintext passwords from memory
- Uses tools like Mimikatz
- Bypass credential isolation
- Educational reference for password recovery

### **[12] Clear Event Logs**
Removes forensic evidence:
- Clears Security event log
- Clears System event log
- Clears Application event log
- Uses wevtutil to suppress logging

### **[13] Disable AV Completely**
Aggressive antivirus disabling:
- PowerShell Set-MpPreference commands
- Disables all Defender features
- Stops AV services
- Removes scheduled scan tasks

### **[14] Show Timeline**
Displays exploitation summary:
- Attack timeline and stages
- System impact assessment
- Detection risks
- Recommended remediation steps

### **[15] EXIT**
Cleanly exits the menu system and program.