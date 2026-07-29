# ✍️ Detailed Walkthrough & Lab Solutions

## Task 1 - Introduction
- **Question:** Read the above and launch the machine.
- **Answer:** *No answer needed.*

---

## Task 2 - Main Components of Metasploit
- **Question 1:** What module is used for covert scanning and enumeration?
  - **Answer:** `auxiliary`
- **Question 2:** What payload type has its code sent in one single piece?
  - **Answer:** `singles`

---

## Task 3 - Msfconsole Commands
- **Question 1:** What command do you use to search for modules?
  - **Answer:** `search`
- **Question 2:** How do you select a module for use?
  - **Answer:** `use`

---

## Task 4 - Exploitation Walkthrough
### Steps Executed:
1. Launched `msfconsole`.
2. Located the exploit module:
   ```bash
   search ms17_010
   use exploit/windows/smb/ms17_010_eternalblue


