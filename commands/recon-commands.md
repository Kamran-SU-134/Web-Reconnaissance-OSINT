# Reconnaissance command reference

Use these commands only within the scope described in the main README.

## Install base tools

```bash
sudo apt update
sudo apt install -y whois dnsutils nmap curl jq git traceroute php-cli
```

## Commands used in this learning lab

```bash
ping -c 4 scanme.nmap.org
traceroute scanme.nmap.org
whois example.com
dig example.com A +short
theHarvester -d example.com -b bing
subfinder -d example.com -silent > subs.txt
curl -s "https://crt.sh/?q=%25.example.com&output=json" | jq -r '.[].name_value' | sort -u
sudo nmap -sS -p 1-1000 -T4 scanme.nmap.org
curl -I http://example.com
```

## Notes

- `ping` and `traceroute` send network traffic to the target.
- WHOIS, DNS, search-engine OSINT, and certificate-transparency lookups are generally passive queries to third-party information services.
- `subfinder` is intended for passive subdomain discovery by default, but always review its current documentation and configuration.
- The Nmap command above is intentionally limited to `scanme.nmap.org` and ports 1–1000.
- Tool output can vary. Preserve your actual output as evidence rather than copying sample results from elsewhere.
