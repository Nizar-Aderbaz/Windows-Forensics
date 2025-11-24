## Investigation Summary - Part 2

### Case Details
- **Case Number**: CF-2025-001
- **Investigator**: NIZAR ADERBAZ
- **Date**: 2025-10-10
- **Target System**: Windows 10 Pro

### Key Findings - User Behavior Analysis
- **Suspicious Activity**: Atomic Red Team folder access and persistence mechanism
- **PowerShell Execution**: 2 executions detected via UserAssist
- **Screenshot Activity**: Snipping Tool used 9 times
- **Persistence Found**: Auto-start entry for AtomicRedTeam.exe in Run registry key
- **Extensive Navigation**: Deep exploration of Atomic Red Team framework folders

### Critical Artifacts Discovered
- **UserAssist**: Application execution history with timestamps
- **RecentDocs**: File and folder access patterns
- **Shellbags**: Folder navigation history including deleted locations
- **Open/Save MRU**: Application-specific file operations
- **Last-Visited MRU**: File association usage patterns

## Tools Used

- **Registry Explorer** - Windows registry analysis and exploration
- **RegRipper** - Automated registry parsing with specialized plugins
- **Notepad++** - Bulk data analysis and pattern searching
- **Timeline Explorer** - Chronological activity visualization

## Investigation Questions Answered

### Application Usage Patterns
- ✅ **PowerShell Activity** → 2 executions detected
- ✅ **Screenshot Tools** → Snipping Tool heavily used (9 times)
- ✅ **System Utilities** → Calculator, Paint, Notepad frequent usage
- ✅ **Security Tools** → Windows Security accessed

### Suspicious Activity Identified
- ⚠️ **Atomic Red Team** → Red team tool folder accessed
- ⚠️ **Persistence Mechanism** → Auto-start registry entry established
- ⚠️ **Extensive Framework Navigation** → Deep exploration of attack tools

### User Behavior Timeline
- **17:14:10** - Initial Atomic Red Team folder access
- **17:17:05** - File dialog activity via PickerHost.exe
- **17:20:51** - Continued Atomic Red Team navigation
- **17:22:50** - PowerShell execution
- **17:41:12** - RecentDocs updates
- **17:41:24** - Network configuration access

## Getting Started

To explore this forensic investigation:
1. Navigate to the `Part-2-User-Behavior-Analysis/` directory
2. Download and review the `Part-2-User-Behavior-Analysis.pdf` file
3. Follow the user behavior analysis methodology documented

## 🎯 Project Goal
To demonstrate practical DFIR skills through real, structured Windows forensic analysis from acquisition to user behavior reconstruction.

---
*For educational and forensic research purposes only*
