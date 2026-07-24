# TryHackMe - Nmap Room Write-up & Solutions

A comprehensive, clean, and organized write-up for the **Nmap** room on TryHackMe. This document covers fundamental network scanning concepts, Nmap switches, scan types, script engine utilization, and firewall evasion tactics.

---

## Task 2: Network Fundamentals & Introduction

* **What networking constructs are used to direct traffic to the right application on a server?**
  `Ports`

* **How many of these are available on any network-enabled computer?**
  `65535`

* **(Research) How many of these are considered "well-known"?**
  `1024`

---

## Task 3: Nmap Switches

* **What is the first switch listed in the help menu for a SYN scan?**
  `-sS`

* **Which switch would you use for a UDP scan?**
  `-sU`

* **If you wanted to detect which operating system the target is running on, which switch would you use?**
  `-O`

* **Nmap provides a switch to detect the version of the services running on the target. What is the switch?**
  `-sV`

* **The default output provided by Nmap often does not provide enough information. How would you increase the verbosity?**
  `-v`

* **Verbosity level one is good, but verbosity level two is better. How would you set the verbosity level to two?**
  `-vv`

* **What switch would you use to save the Nmap results in three major formats?**
  `-oA`

* **What switch would you use to save the Nmap results in a "Normal" format?**
  `-oN`

* **A very useful format, how would you save results in a "grepable" format?**
  `-oG`

* **How would you activate "aggressive" mode (enables service detection, OS detection, traceroute, and common script scanning)?**
  `-A`

* **How would you set the timing template to level 5?**
  `-T5`

* **How would you tell Nmap to only scan port 80?**
  `-p 80`

* **How would you tell Nmap to scan ports 1000-1500?**
  `-p 1000-1500`

* **How would you tell Nmap to scan all ports?**
  `-p-`

* **How would you activate a scan without pinging the host?**
  `-Pn`

---

## Task 4: Scan Types - Overview & TCP Connect Scans

* **Which RFC defines the appropriate behaviour for the TCP protocol?**
  `RFC 793`

* **If a port is closed, which flag should the server send back to indicate this?**
  `RST`

---

## Task 5: SYN Scans

* **There are two other names for a SYN scan, what are they?**
  `Half-Open, Stealth`

* **Can Nmap run a SYN scan without sudo permissions (as a non-root user)? (Y/N)**
  `N`

---

## Task 6: UDP Scans

* **If a UDP port doesn't respond to an Nmap scan, what will it be marked as?**
  `open|filtered`

* **When a UDP port is closed, by convention the target should send back a "port unreachable" message. Which protocol would it use to do so?**
  `ICMP`

---

## Task 7: NULL, FIN & Xmas Scans

* **Which of the three shown scan types uses the URG flag?**
  `Xmas`

* **Why are NULL, FIN, and Xmas scans generally used?**
  `Firewall Evasion`

* **Which common OS may respond to NULL, FIN, and Xmas scans with a RST for every port?**
  `Microsoft Windows`

---

## Task 8: Ping Sweep Scans

* **How would you perform a ping sweep on the 172.16.x.x network (Netmask 255.255.0.0) using Nmap in CIDR notation?**
  `nmap -sn 172.16.0.0/16`

---

## Task 9: Working with the NSE (Nmap Script Engine)

* **What language are NSE scripts written in?**
  `Lua`

* **Which category of scripts would be a very bad idea to run in a production environment?**
  `exploit`

---

## Task 10: Searching for Scripts

* **What optional argument can the `ftp-anon.nse` script take?**
  `maxlist`

---

## Task 11: Script Import & DB Updates

* **Search for "smb" scripts in the `/usr/share/nmap/scripts/` directory. What is the filename of the script which determines the underlying OS of the SMB server?**
  `smb-os-discovery.nse`

* **Read through this script. What does it depend on?**
  `smb-brute`

---

## Task 12: Firewall Evasion

* **Which Nmap switch allows you to append an arbitrary length of random data to the end of packets?**
  `--data-length`

* **Which switch allows you to spoof your IP address?**
  `-S`

* **Which switch allows you to spoof your MAC address?**
  `--spoof-mac`

---

## Task 13: Practical / Conclusion

* **Does the target IP respond to ICMP echo (ping) requests? (Y/N)**
  `N`

* **Perform an Xmas scan on the first 999 ports of the target. How many ports are shown to be open or filtered?**
  `999`

* **Perform a TCP SYN scan on the first 5000 ports of the target. How many ports are shown to be open?**
  `5`

* **Deploy the `ftp-anon` script against the box. Can Nmap login successfully to the FTP server on port 21? (Y/N)**
  `Y`
