## Available Reports

### Part 1: Acquisition & Triage
- **File**: `Part-1-Acquisition-Triage.pdf`
- **Location**: `/Part-1-Acquisition-Triage/`
- **Focus**: Memory and disk acquisition, forensic triage, registry analysis

## Investigation Summary - Part 1

### Case Details
- **Case Number**: CF-2025-001
- **Investigator**: NIZAR ADERBAZ
- **Date**: 2025-11-11
- **Target System**: Windows 10 Pro

### Key Findings
- **Active Account During Attack**: KR3L_DF
- **Newly Created Suspicious Account**: art-test (created 30 minutes after initial compromise)
- **Administrator Group Members**: 3 SIDs identified with administrative privileges
- **User Profiles**: KR3L_DF profile identified on system

### Forensic Procedures Covered
1. **Memory Acquisition** using VBoxManage
2. **Disk Imaging** with forensic integrity verification
3. **Disk Mounting** using Arsenal Image Mounter
4. **Automated Triage** with KAPE
5. **Registry Analysis** using Registry Explorer and RegRipper

## Tools Used

- **VirtualBox & VBoxManage** - VM management and evidence acquisition
- **FTK Imager** - Disk imaging and forensic analysis
- **Arsenal Image Mounter** - Mounting disk images for analysis
- **KAPE** - Automated forensic triage and artifact collection
- **Registry Explorer** - Windows registry analysis and exploration
- **RegRipper** - Automated registry parsing and data extraction
- **Notepad++** - Log analysis and text file examination

## Investigation Questions Answered

- ✅ **Active accounts during attack timeframe** → KR3L_DF
- ✅ **Accounts created** → art-test (suspicious backdoor account)
- ✅ **Administrator group members** → 3 SIDs identified
- ✅ **Users with profiles** → KR3L_DF

## Getting Started

To explore this forensic investigation:
1. Navigate to the `Part-1-Acquisition-Triage/` directory
2. Download and review the `Part-1-Acquisition-Triage.pdf` file
3. Follow the step-by-step forensic procedures documented


## 🎯 Project Goal
To demonstrate practical DFIR skills through real, structured Windows forensic analysis from acquisition to evidence interpretation.

---
*For educational and forensic research purposes only*
