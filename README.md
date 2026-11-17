# Reviewing-Unallocated-Space-Extracting-Data-with-Tools-Digital-Investigation-Processes
## AIM:
To review unallocated space in a disk image, extract data using forensic tools, and understand the digital investigation process.
## REQUIREMENTS
- Autopsy or FTK Imager
- Sleuth Kit (TSK)
- Hex Editor (e.g., HxD)
- Operating System: Windows 10/11 or Linux (Kali preferred)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Load into Autopsy or Sleuth Kit]
    B --> C[Identify Unallocated Space]
    C --> D[Scan for Data Signatures]
    D --> E[Carve and Recover Files]
    E --> F[Analyze Recovered Data]
    F --> G[Document Findings in Report]
```
## DESIGN STEPS:
### Step 1 (Acquire Evidence Image):
- Obtain the disk image in ```.dd``` or ```.E01``` format from a trusted forensic acquisition process.
- Verify hash values (MD5/SHA256) to maintain integrity.

### Step 2(Load Image into Forensic Tool):
- Open Autopsy or FTK Imager.
- Create a new case and add the evidence image.

### Step 3(Locate Unallocated Space):
- Navigate to the partition structure view.
- Identify sectors not assigned to any partition (unallocated).
### Step 4(Analyze & Carve Data):
- Use built-in data carving tools to search for file signatures (JPEG, DOCX, PDF, etc.).
- Preview carved files for relevance.
  
## PROGRAM:
| Step | Action                     | Tool Used                   | Output                       |
| ---- | -------------------------- | --------------------------- | ---------------------------- |
| 1    | Load disk image            | Autopsy / FTK Imager        | Partition & unallocated view |
| 2    | Identify unallocated space | Autopsy File System View    | Sector ranges                |
| 3    | Data carving               | Autopsy Data Carving Module | Recovered files              |
| 4    | Export evidence            | Autopsy Export Option       | File copies for analysis     |


## OUTPUT:
Unallocated Space Analysis and Extracted Data Report

<img width="1917" height="1020" alt="Screenshot 2026-11-17 100938" src="https://github.com/user-attachments/assets/cabb728a-2a8c-4357-87ed-05dada18894c" />

<img width="1916" height="1020" alt="Screenshot 2026-11-17 101000" src="https://github.com/user-attachments/assets/68b1c4e8-9864-4688-b6d6-ca0a0c1ded25" />

<img width="1915" height="1005" alt="Screenshot 2026-11-17 101214" src="https://github.com/user-attachments/assets/114fc530-d6bf-4bc5-b83e-e2aa437b5fbf" />


<img width="1912" height="1002" alt="Screenshot 2026-11-17 143617" src="https://github.com/user-attachments/assets/a90f0efa-37ce-46a2-a3f0-052c7f7b0703" />


## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

