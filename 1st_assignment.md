# Assignment 6: What is Shodan?
---

## 1. Introduction
Shodan is a specialized search engine often referred to as the **"Google for Hackers"**.  
Unlike traditional search engines that index web pages, Shodan indexes **devices and services** connected to the internet.  
It scans for **open ports**, **service banners**, **software versions**, and other metadata that can be useful for both attackers and defenders.

---

## 2. Objective of the Assignment
The purpose of this task is to:
- Search for `scanme.nmap.org` on Shodan.
- Identify and document the publicly available information.
- Explain how such information could be useful for attackers and defenders.
- Provide supporting screenshots.

---

## 3. Steps Taken

1. **Searched for `scanme.nmap.org` on Shodan**  
   - Result: **No results found**  
   ![Screenshot 1: Shodan search for scanme.nmap.org](screenshots/screenshot1.png)

2. **Resolved the hostname to its IP address using nslookup**  
   - IPv6: `2600:3c01::f03c:91ff:fe18:bb2f`  
   - IPv4: `45.33.32.156`  
   ![Screenshot 2: terminal nslookup addres for scanme.nmap.org](Screenshots/screenshot2.png)
   ![Screenshot 3: nslookup result for scanme.nmap.org](Screenshots/screenshot3.png)

---

## 4. Observations
- Shodan did not return any results for either the hostname or the IP address.
- This could be due to:
  - Shodan not having scanned this IP recently.
  - The target host being excluded from Shodan's indexing.
  - Dynamic changes in IP or server configuration.

---

## 5. Limitations of Shodan
- Shodan does not scan in **real-time**; it relies on periodic scans.
- Some devices and servers may **block Shodan's scanning IP ranges**.
- If a device is **newly connected or rarely online**, it may not appear in Shodan's results.

---

## 6. How This Information Could Be Used

### For Attackers
- Identify **open ports** and services.
- Detect **outdated software versions** that may have known vulnerabilities.
- Plan targeted attacks such as **brute-force SSH login** or **SQL injection**.

### For Defenders
- Audit and **discover exposed services**.
- Patch or update outdated services to **reduce vulnerability**.
- Monitor for **unexpected changes** in publicly exposed devices.

---

## 7. Conclusion
In this assignment, Shodan was used to attempt to gather information on `scanme.nmap.org`.  
While no results were found, this demonstrates an important point: **Shodan’s usefulness depends on the availability of recent indexed data**.  
Even without results, understanding how Shodan works is valuable for both **security assessment** and **attack surface monitoring**.

--- 
