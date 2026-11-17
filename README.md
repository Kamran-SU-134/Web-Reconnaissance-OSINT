# 🔎 Web Reconnaissance & OSINT Information Gathering

## 📌 Project Overview

This project demonstrates practical reconnaissance and Open-Source Intelligence (OSINT) techniques using Kali Linux.

The objective is to understand how cybersecurity professionals collect publicly available information about a target domain, analyze DNS records, discover subdomains, identify network services, and inspect web server information.

## 🎯 Project Objectives

- Perform domain reconnaissance.
- Collect WHOIS information.
- Identify DNS records and IP information.
- Discover publicly available subdomains.
- Perform certificate transparency searches.
- Conduct basic network port scanning.
- Analyze HTTP response headers.
- Explore automated reconnaissance using RED_HAWK.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Security testing environment |
| WHOIS | Domain registration information |
| DIG | DNS record enumeration |
| Nmap | Network and port scanning |
| Ping | Connectivity testing |
| Traceroute | Network path analysis |
| theHarvester | OSINT information gathering |
| Subfinder | Subdomain discovery |
| crt.sh | Certificate transparency lookup |
| cURL | HTTP header analysis |
| RED_HAWK | Automated reconnaissance |
| jq | JSON processing |

## ⚙️ Installation

Update Kali Linux:

```bash
sudo apt update && sudo apt upgrade -y
```

Install required tools:

```bash
sudo apt install -y whois dnsutils nmap curl jq git php-cli traceroute
```

## 🔍 Practical Reconnaissance Commands

### 1. Network Connectivity

```bash
ping -c 4 scanme.nmap.org
```

### 2. Traceroute

```bash
traceroute scanme.nmap.org
```

### 3. WHOIS Enumeration

```bash
whois example.com
```

### 4. DNS Enumeration

```bash
dig example.com A +short
```

### 5. OSINT with theHarvester

```bash
theHarvester -d example.com -b bing
```

### 6. Subdomain Discovery

```bash
subfinder -d example.com -silent > subs.txt
```

### 7. Certificate Transparency Search

```bash
curl -s "https://crt.sh/?q=%25.example.com&output=json" | jq '.[].name_value' | sort -u
```

### 8. Nmap Port Scanning

```bash
sudo nmap -sS -p 1-1000 -T4 scanme.nmap.org
```

### 9. HTTP Header Analysis

```bash
curl -I http://example.com
```

### 10. Automated Reconnaissance with RED_HAWK

Clone the repository:

```bash
git clone https://github.com/Tuhinshubhra/RED_HAWK.git
```

Navigate into the directory:

```bash
cd RED_HAWK
```

Run the tool:

```bash
php rhawk.php -i example.com
```

## 📊 Expected Learning Outcomes

- Understanding passive and active reconnaissance.
- Understanding DNS and WHOIS information.
- Learning subdomain enumeration techniques.
- Understanding network scanning with Nmap.
- Analyzing HTTP response headers.
- Using multiple Kali Linux reconnaissance tools.
- Understanding basic OSINT workflows.

## 📸 Project Evidence

Screenshots of terminal commands and their results are available in the `screenshots/` directory.

## 🔐 Ethical Disclaimer

This project is intended for educational purposes and authorized security testing only.

- Only test domains and systems you own or have explicit permission to assess.
- Use approved scanning targets such as Nmap's ScanMe service within its stated testing scope.
- Do not perform unauthorized vulnerability scanning.
- Publicly available information does not automatically grant permission to test a system.

## 👨‍💻 Author

Cybersecurity Student | Aspiring SOC Analyst | Blue Team & Security Research Enthusiast

**GitHub:**https://github.com/Kamran-SU-134

**LinkedIn:** https://www.linkedin.com/in/kamran-khan-325590371/

---

⭐ If you find this project useful, consider giving it a star!
