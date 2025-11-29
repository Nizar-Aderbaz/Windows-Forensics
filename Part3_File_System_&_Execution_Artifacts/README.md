# Investigation Summary - Part 3

## Case Details
- **Case Number:** CF-2025-001  
- **Investigator:** NIZAR ADERBAZ  
- **Date:** 2025-10-10  
- **Target System:** Windows 10 Pro  

---

## Advanced Artifacts Analyzed

### **File System Artifacts**
- **Master File Table (MFT):** Complete file system metadata analysis  
- **USN Journal:** File system change tracking  
- **Background Activity Moderator (BAM):** Background process tracking  
- **AppCompatCache / Shimcache:** Application compatibility records  
- **AmCache:** Program execution metadata  
- **Prefetch:** Application startup optimization data  

---

## Tools Used
- **MFTECmd** – MFT and USN Journal parsing  
- **Timeline Explorer** – Chronological analysis  
- **Registry Explorer** – Registry analysis  
- **PECmd** – Prefetch analysis  
- **AmcacheParser** – AmCache analysis  
- **Notepad++** – Bulk data review  

---

## Critical Findings

### **MFT Analysis – Atomic Red Team Evidence**
- **Files Discovered:**  
  `Invoke-atomicredteam`, `Get-AtomicTechnique.ps1`, `Install-atomicredteam.ps1`, `Phant0m.exe`
- **ART-attack.ps1 MFT Entry:** `111159`
- **MACB Timestamps:**  
  - **Modified:** 2024-10-10 17:31:47  
  - **Accessed:** 2025-10-10 17:31:43  

---

### **USN Journal – Rapid File Operations**
- **File:** `deleteme_T1551.004`  
- **Created:** 17:39:42  
- **Deleted:** 17:39:48 (**6-second lifespan**)  
- **Entry Number:** 112466  
- **Status:** File deleted, MFT entry not in use  

---

### **AmCache – Malware Identification**
- **Malware Hash:** `c51217ce3d1959e99886a567d21d0b97022bd6e3` (AtomicService.exe)  
- **VirusTotal:** Confirmed malicious  

---

### **Prefetch – Execution Confirmation**
- **Executed Binary:** `ATOMICSERVICE.EXE`  
- **Execution Time:** 2025-10-10 17:37:43  
- **Location:** `\ATOMICREDTEAM\TMP\...\ATOMICS\T1543.003\BIN\`  
- **Additional:** Multiple CMD/PowerShell executions detected  

---

## Investigation Questions Answered

### **File Location & Identification**
- Atomic Red Team directory contained multiple attack tools  
- **Relevant Entry:** ART-attack.ps1 — MFT Entry `111159`  

---

### **Timestamp Analysis**
- MACB timestamps show normal system behavior  
- **No timestomping detected**  

---

### **Deleted File Investigation**
- **Created:** 2025-10-10 17:39:42  
- **Deleted:** 2025-10-10 17:39:48  
- **Entry:** 112466  
- **Status:** Fully deleted from MFT  

---

## Key Evidence Uncovered

### **Definitive Attack Confirmation**
- Atomic Red Team tools were executed  
- Service-based persistence attempt (**T1543.003**) detected  
- Malware confirmed via VirusTotal  
- Rapid anti-forensic file operations identified  

---

## Execution Timeline

- 17:37:43 - ATOMICSERVICE.EXE execution
- 17:39:42 - Suspicious file creation
- 17:39:48 - Rapid file deletion

### **For educational and forensic research purposes only**


