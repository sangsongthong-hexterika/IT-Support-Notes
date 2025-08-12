# Backup & Recovery Setup – Mock Report

**Client:** ExampleCo  
**Date:** DD Month YYYY  
**Report Author:** Sangsongthong Chantaranothai – Hexterika Cyberlab  
**Engagement Type:** File-level backup setup & recovery test  
**Status:** Mock report – for portfolio purposes only  

---

## 1. Confidentiality Statement

This document is the property of ExampleCo and Hexterika Cyberlab. It contains information intended for the client and their approved stakeholders. Distribution outside of this scope requires written consent.

---

## 2. Scope

**In Scope:**

- File-level backup configuration for selected folders
- Automated sync to both local & cloud targets  
- Test restore to confirm file integrity  
- One-page recovery guide for client

**Out of Scope:**

- Full system imaging or bare-metal recovery  
- Database backup solutions  
- Cloud-native backup configuration (e.g., AWS Backup, Azure Recovery Services)  

---

## 3. Tools Used

- **rsync** (Linux/Mac) – CLI-based sync tool  
- **FreeFileSync** (Windows/Linux/Mac) – GUI-based sync tool  
- **Google Drive / Dropbox / OneDrive** – cloud sync targets  
- **VM snapshot (optional)** – for safe restore testing

---

## 4. Methodology

1. **Requirements Gathering** – Identified client’s data priorities, storage limits, and recovery goals.  
2. **Backup Configuration** – Created scheduled sync job from source folders to:
   - Local external drive
   - Cloud storage folder
3. **Verification** – Manually reviewed backup logs for errors or skipped files.  
4. **Restore Test** – Selected sample files restored to an alternate location and opened to confirm integrity.  
5. **Recovery Documentation** – Provided client with a one-page quick guide on restoring from local and cloud backups.

---

## 5. Findings

| Finding ID | Description | Impact | Recommendation |
|------------|-------------|--------|----------------|
| BR-001 | No backup versioning in current setup | Medium | Enable version history in cloud storage or use versioning-capable software |
| BR-002 | External drive stored in same physical location | High | Store backups in a different physical location to prevent loss from fire/theft |

---

## 6. Recommendations

- **Enable cloud backup versioning** to recover from accidental deletions or overwrites.  
- **Rotate physical drives** monthly and store offsite.  
- **Review backup logs weekly** to catch sync errors early.  

---

## 7. Recovery Test Results

| File/Folder | Backup Source | Restore Destination | Status |
|-------------|--------------|--------------------|--------|
| /Documents | Google Drive | /Restored/Docs | Success |
| /Photos | External HDD | /Restored/Photos | Success |

---

## 8. Conclusion

The configured backup setup provides **basic redundancy** via local and cloud storage, with successful restore tests confirming file integrity. Risk remains from lack of versioning and same-location storage — implementing the above recommendations will improve resilience.

---

## 9. Appendix

**Recovery Guide (Example):**  

1. Open FreeFileSync.  
2. Select “Restore Job – [Job Name]”.  
3. Confirm destination folder and click “Start”.  
4. For Google Drive:
   - Log in → My Drive → locate folder → download required files.

---
