# Cybersecurity Week 2 Project
### Footprinting, Reconnaissance and Network Scanning Using Kali Linux

![Kali Linux](https://img.shields.io/badge/Platform-Kali%20Linux-blue?logo=kalilinux)
![Nmap](https://img.shields.io/badge/Network%20Scanning-Nmap%207.97-green)
![Maltego](https://img.shields.io/badge/Tool-Maltego-orange)
![Project](https://img.shields.io/badge/Project-Cybersecurity-purple)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)

## 📌 Project Overview

This repository contains the practical implementation of cybersecurity footprinting, reconnaissance, information gathering and network scanning activities performed as part of the Week 2 Cybersecurity Project.

The project focuses on understanding how cybersecurity professionals collect publicly available information about domains, identify digital footprints, analyse DNS infrastructure, discover relationships between domain entities and perform network scanning using industry-standard tools.

All practical activities were performed using Kali Linux in a virtualised environment.

## 🎯 Project Objectives

- Understand the fundamentals of footprinting and reconnaissance.
- Explore publicly available information using Kali Linux tools.
- Learn Google Hacking Database (GHDB) search techniques.
- Perform domain-based footprinting using Maltego.
- Collect publicly available domain information using theHarvester.
- Understand network scanning using Zenmap and Nmap.
- Analyse and document findings through screenshots and terminal logs.
- Develop practical knowledge of ethical cybersecurity assessment.

## 🛠️ Tools and Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Cybersecurity testing environment |
| WHOIS | Domain registration information |
| WhatWeb | Website technology identification |
| NSLOOKUP | DNS record lookup |
| cURL | HTTP response and header analysis |
| WAFW00F | Web Application Firewall identification |
| DNSRecon | DNS enumeration |
| GHDB | Google search operators and footprinting |
| Maltego | Visual link analysis and domain footprinting |
| theHarvester | Public information gathering |
| Zenmap | Graphical network scanning interface |
| Nmap 7.97 | Network discovery and port scanning |

## 📂 Project Structure

```text
Cybersecurity-Week2-Project/
│
├── PM1-Kali-Footprinting/
│   ├── screenshots/
│   └── logs/
│
├── PM2-GHDB/
│   ├── screenshots/
│   └── logs/
│
├── PM3-Maltego/
│   ├── screenshots/
│   ├── logs/
│   └── PM3_Maltego_Footprinting.mtgx
│
├── PM4-theHarvester/
│   ├── screenshots/
│   └── logs/
│
├── PM5-Zenmap/
│   ├── screenshots/
│   └── logs/
│
└── README.md
```

*Note: The structure above represents the intended organisation. Only folders and files actually completed and saved are included in the repository.*

---

## 🔍 PM1 – Footprinting Using Kali Linux Tools

### Objective
To understand how different Kali Linux tools can be used to gather publicly available information about a target domain.

### Tools Used

**1. WHOIS**

Used to collect domain registration information, including registrar details, registration dates, name servers and domain status.

**2. WhatWeb**

Used to identify website technologies and components.

**3. NSLOOKUP**

Used to retrieve DNS information such as NS, MX and TXT records.

**4. cURL**

Used to inspect HTTP response headers and understand server responses.

**5. WAFW00F**

Used to identify the presence of a Web Application Firewall.

**6. DNSRecon**

Used to perform DNS enumeration and collect DNS-related information.

### Key Observations

- Domain registration and registrar information was retrieved.
- DNS name servers and mail exchange records were identified.
- HTTP response headers were examined.
- ModSecurity (SpiderLabs) was identified by WAFW00F.
- DNSRecon returned DNS records and related infrastructure information.

### Evidence

Screenshots and command outputs are maintained in the PM1 evidence folders.

---

## 🌐 PM2 – Google Hacking Database (GHDB)

### Objective
To understand Google search operators and how publicly indexed information can be discovered through advanced search techniques.

### Activities Performed

- Explored the Google Hacking Database.
- Studied different GHDB categories.
- Used the `site:` operator to identify indexed pages.
- Used `filetype:` to search for indexed PDF documents.
- Used `inurl:` to identify pages with specific URL patterns.
- Used `intitle:` to search pages with specific titles.
- Used `intext:` to search for specific text within indexed pages.

### Sample Google Dorks

```text
site:networkwalks.com

site:networkwalks.com filetype:pdf

site:networkwalks.com inurl:blog

site:networkwalks.com intitle:documentation

site:networkwalks.com intext:privacy policy
```

### Key Observations

- Explored multiple Google Hacking Database categories.
- Tested different Google search operators.
- Observed that some queries returned no matching indexed documents.
- Documented search results and no-result observations.

### Evidence

Screenshots of GHDB exploration and Google search results are maintained in PM2.

---

## 🕸️ PM3 – Maltego-Based Footprinting

### Objective
To perform domain-based footprinting and visualise relationships between domain infrastructure components.

### Activities Performed

- Installed and configured Maltego Community Edition.
- Created a new Maltego graph.
- Added `networkwalks.com` as a Domain entity.
- Executed DNS-related transforms.
- Observed relationships between domain entities.

### Key Findings

The Maltego graph identified:

- Domain: `networkwalks.com`
- DNS names: `mail.networkwalks.com` and `webmail.networkwalks.com`
- MX record: `mail.networkwalks.com`
- Name servers:
  - `ns6135.hostgator.com`
  - `ns6136.hostgator.com`

### Evidence

The Maltego graph and transform results are included in the PM3 screenshots and project files.

---

## 📡 PM4 – theHarvester-Based Footprinting

### Objective
To understand how publicly available information can be collected using theHarvester and supported data sources.

### Activities Performed

- Verified theHarvester installation in Kali Linux.
- Performed a Certificate Transparency lookup using CRT.sh.
- Attempted an additional lookup using DuckDuckGo.
- Recorded the results in terminal logs.

### Command Used

```bash
theHarvester -d networkwalks.com -b crtsh
```

### CRT.sh Results

| Information | Result |
|---|---|
| Target | networkwalks.com |
| Source | CRT.sh |
| IP addresses | None found |
| Email addresses | None found |
| People | None found |
| Hosts | None found |

The CRT.sh lookup completed without identifying matching results.

### Evidence

Command outputs and screenshots are maintained in PM4.

---

## 🖥️ PM5 – Network Scanning Using Zenmap

### Objective
To understand network scanning and host information analysis through Zenmap, the graphical interface for Nmap.

### Activities Performed

- Verified Nmap/Zenmap version 7.97.
- Launched the Zenmap graphical interface.
- Configured a Quick Scan.
- Used `127.0.0.1` as the scan target to examine the local Kali machine.
- Explored scan output and discovered services.

### Key Concepts

- Host discovery
- Port scanning
- Service identification
- Nmap output analysis
- Host details
- Network topology visualisation

### Evidence

Zenmap screenshots and saved scan outputs are maintained in PM5.

---

## 📊 Project Learnings

Through these practical exercises, the project provided hands-on exposure to:

1. Domain registration and DNS information gathering.
2. Website technology identification.
3. HTTP response and security header analysis.
4. Web Application Firewall detection.
5. Google search operators and publicly indexed information.
6. Visual reconnaissance through Maltego.
7. Public information collection through theHarvester.
8. Network scanning and service discovery using Zenmap.

## ⚠️ Limitations

- Results depend on the availability of public information sources.
- Search engines may not index every publicly accessible page.
- Some tools may return limited results depending on their data sources.
- DNS and footprinting results can change over time.
- The project does not establish that a target is vulnerable merely because information is publicly available.

## 🔮 Future Enhancements

- Include additional passive reconnaissance tools.
- Improve automation of information gathering.
- Generate consolidated reconnaissance reports.
- Explore additional DNS and network analysis techniques.
- Integrate findings into a structured cybersecurity assessment workflow.
- Expand practical exercises using dedicated authorised lab environments.

## 🔐 Ethical Considerations and Disclaimer

This project is intended strictly for educational and cybersecurity learning purposes.

- Perform security testing only on systems you own or have explicit authorisation to assess.
- Do not access, download or disclose private or sensitive information.
- Do not use discovered information for unauthorised activities.
- Respect applicable cybersecurity laws, privacy requirements and responsible disclosure practices.

The tools and techniques demonstrated in this repository should be used responsibly.

## 👨‍💻 Author

**Prashant Dubey**

Cybersecurity Enthusiast | Computer Science Engineering Student

GitHub: [Add your GitHub profile link]

LinkedIn: [Add your LinkedIn profile link]

---

⭐ If you find this project useful for learning cybersecurity footprinting and reconnaissance, consider giving the repository a star.
