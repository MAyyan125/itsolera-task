# itsolera-task

ReconTool - Lightweight Reconnaissance CLI Utility Author: Mr.Ayyan Irfan
Last Updated: June 2025

Overview
ReconTool is a lightweight and modular command-line tool for automating initial reconnaissance tasks during penetration testing. It supports WHOIS lookups, DNS and subdomain enumeration, port scanning, banner grabbing, and technology detection.
This tool is intended for educational and ethical hacking purposes only.

Features
- WHOIS lookup for domain registration information - DNS record enumeration (A, NS, MX, TXT)
- Subdomain enumeration using crt.sh
- Fast port scanning using nmap
- Banner grabbing for service identification
- Technology detection using WhatWeb
- Optional output saving support (basic)

Requirements
Make sure the following Python modules and tools are installed:
Python Modules (install via pip):
pip install python-whois requests python-nmap dnspython

System Tools:
- nmap - for port scanning and banner grabbing
- WhatWeb - for detecting web technologies Install via:
sudo apt install whatweb
Usage
python recontool.py [OPTIONS]
Options
- -w, --whois_lookup : Perform WHOIS lookup on domain
- -d, --dns
- -s, --sub
- -p, --port
- -b, --banner
- -t, --techdetect - --output
: Perform DNS enumeration : Subdomain enumeration
: Port scanning using nmap
: Banner grabbing with nmap -sV
: Detect technologies using WhatWeb
: Save output to file (feature placeholder)
Examples

# WHOIS Lookup
python recontool.py -w example.com
# DNS Enumeration
python recontool.py -d https://example.com
# Subdomain Enumeration
python recontool.py -s example.com
# Fast Port Scan
python recontool.py -p 93.184.216.34
# Banner Grabbing
python recontool.py -b 93.184.216.34
# Technology Detection
python recontool.py -t https://example.com
Notes
- Ensure nmap and whatweb are installed and accessible in your system's PATH. - Use a VPN or proper authorization when scanning external networks.
- Output saving via --output is defined in the parser but currently not implemented.
License
This project is released under the MIT License. Use responsibly.
Disclaimer
This tool is for authorized testing and educational use only. Unauthorized use may violate laws and result in severe penalties. Always get proper permission before scanning any system.
