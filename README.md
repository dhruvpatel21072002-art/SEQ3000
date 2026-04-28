# SEQ3000 – COBOL File Maintenance

**Author:** Dhruv Patel  
**GitHub:** https://github.com/dhruvpatel21072002-art/SEQ3000  

---

## Overview
This project demonstrates how to maintain an employee master file using COBOL. It includes both **sequential file processing** and **indexed file processing** techniques to handle real-world data updates.

The programs perform operations such as adding, updating, and deleting employee records using a transaction file.

---

## Programs Included

### SEQ3000 (Sequential File Maintenance)
This program updates a sequential master file by comparing it with a transaction file.

- Reads transaction file (EMPTRAN) and old master file (OLDEMP)
- Writes updated records to NEWEMP
- Writes invalid transactions to ERRTRAN3

It uses a merge logic with switches to control reading and processing records.

---

### EMPIND01 (Indexed File Creation)
This program creates an indexed file from the sequential master file.

- Converts OLDEMP into EMPMASTI (indexed file)
- Uses employee ID as the key for faster access

---

### EMPIND02 (Indexed File Maintenance)
This program updates the indexed file directly.

- Uses random access instead of sequential reading
- Applies Add, Change, and Delete operations
- Writes errors to a separate file

---

## Input Files

- **OLDEMP** – Original employee master file  
- **EMPTRAN** – Transaction file  
  - A = Add  
  - C = Change  
  - D = Delete  

---

## JCL
JCL is used to compile and run each program on the mainframe environment.

---

## Key Concepts Learned
- Sequential file merge processing  
- Use of switches to control program flow  
- Indexed file structure and random access  
- File handling and error processing in COBOL  

---

## Summary
This project helped me understand how file maintenance works in COBOL. Sequential processing was more complex, especially with switches and merge logic, while indexed file processing was easier to understand because of direct access using keys. Overall, this project gave me practical experience with real data processing techniques.
