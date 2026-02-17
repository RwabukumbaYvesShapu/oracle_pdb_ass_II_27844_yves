# oracle_pdb_ass_II_27844_yves
# Oracle Database PDB Management - Assignment II

##My Information

- **Name:** Rwabukumba Yves Shapu  
- **Student ID:** 27844  
- **Course:** Database Development with PL/SQL (INSY 8311)  
- **Institution:** Adventist University of Central Africa (AUCA)  
- **Date:** February 2026

---

## Assignment Overview

This assignment demonstrates Oracle Database administration skills including creating and managing Pluggable Databases (PDBs) and configuring Oracle Enterprise Manager (OEM).

---

##Repository Structure
oracle-pdb-assignment-27844-Yves
│
├── README.md                     # This file
├── queries/                      # SQL scripts
│   ├── task1_create_pdb.sql
│   ├── task2_delete_pdb.sql
│   └── task3_oem_setup.sql
│
└── screenshots/                  # Visual documentation
├── task1_creation/           # Task 1 screenshots
├── task2_deletion/           # Task 2 screenshots
└── task3_oem/                # Task 3 screenshots
text

---

##Tasks Completed

### Task 1: Create Main Pluggable Database (2 points)

Created permanent PDB for class work:  
- **PDB Name:** `ry_pdb_27844`  
- **Username:** `yves_plsqlauca_27844`  
- **Password:** `1234`  
- **Location:** D:\PL-SQL\ORADATA\XE\ry_pdb_27844\


**Key Steps:**
1. Connected as SYSDBA to root container  
2. Created PDB from PDB$SEED template  
3. Opened PDB and saved state  
4. Created user with full privileges  

---

### Task 2: Create and Delete PDB (2 points)

Demonstrated PDB lifecycle management:  
- **PDB Name:** `ry_to_delete_pdb_27844`  
- **Status:** Successfully created and permanently deleted

**Key Steps:**
1. Created temporary PDB  
2. Opened and verified existence  
3. Closed PDB for safe deletion  
4. Unplugged PDB (created XML metadata)  
5. Dropped PDB with all datafiles  
6. Verified complete removal  

---

### Task 3: Oracle Enterprise Manager Setup (1 point)

Configured OEM for database monitoring:  
- **HTTP Port:** 1521
- **HTTPS Port:** 5500
- **Access URL:** `https://localhost:5500/em`  
- **Login:** system / 1234

**Key Steps:**
1. Checked and set HTTP/HTTPS ports  
2. Restarted database  
3. Accessed OEM dashboard  
4. Verified all PDBs visible  

---

##Technical Environment

- **OS:** Windows 10/11  
- **Database:** Oracle 21c Express Edition  
- **Instance:** XE  
- **Base Path:** `D:\PL-SQL\ORADATA\XE\`  
- **Tool:** SQL*Plus

---

## 📊 Results Summary

| Task | Description              | Status        | 
|------|--------------------------|---------------|
| 1    | Create Main PDB          | ✅ Complete   |
| 2    | Create & Delete PDB      | ✅ Complete   |
| 3    | Configure OEM            | ✅ Complete   |


---

##Key Concepts Applied

- **CDB (Container Database):** Main database managing multiple PDBs  
- **PDB (Pluggable Database):** Self-contained, portable database units  
- **Multitenant Architecture:** Efficient resource sharing across PDBs  
- **User Management:** Creating users and assigning privileges  
- **OEM:** Database monitoring and management tool

---

##Challenges & Solutions

**Challenge 1:** Finding correct datafile paths  
**Solution:** Queried `CDB_DATA_FILES` to identify existing structure

**Challenge 2:** Selecting unplug directory  
**Solution:** Used `DATA_PUMP_DIR` from `dba_directories` query

**Challenge 3:** OEM port configuration  
**Solution:** Set custom ports (5500) and restarted database

---

sqlplus sys as sysdba
@queries/task1_create_pdb.sql
@queries/task2_delete_pdb.sql
@queries/task3_oem_setup.sql
##VIDEO REFERENCES
https://youtu.be/clTLONpAxOE
