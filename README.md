# Network Scanner

     _   _      _                      _          _____                                 
    | \ | |    | |                    | |        / ____|                                
    |  \| | ___| |___      _____  _ __| | __    | (___   ___ __ _ _ __  _ __   ___ _ __ 
    | . ` |/ _ \ __\ \ /\ / / _ \| '__| |/ /     \___ \ / __/ _` | '_ \| '_ \ / _ \ '__|
    | |\  |  __/ |_ \ V  V / (_) | |  |   <      ____) | (_| (_| | | | | | | |  __/ |   
    |_| \_|\___|\__| \_/\_/ \___/|_|  |_|\_\    |_____/ \___\__,_|_| |_|_| |_|\___|_|   
                                                                                                                                                                        

A simple Python 3 network scanner for local network discovery. The tool performs ARP-based scanning to list live hosts and their MAC addresses. Intended for lab and authorized network assessment use only.

This program is supported for Linux, Windows and Mac OS X.

## Features
- Scan a single IP, CIDR (e.g. 192.168.1.0/24) or an IP range
- Resolves MAC addresses using ARP
- Cross-platform: Linux, Windows, macOS
- Minimal dependencies: scapy, termcolor

## Installation
```bash
git clone https://github.com/jjj-abdulaziz/Network-scanner.git
cd Network-scanner
python3 -m venv .venv
source .venv/bin/activate      # on Windows: .venv\Scripts\activate
pip install -r requirements.txt

# show help
python3 networkscanner.py --help

# scan a CIDR
python3 networkscanner.py --range 192.168.1.0/24

# scan an IP range
python3 networkscanner.py --range 192.168.1.10-192.168.1.50

# scan a single IP
python3 networkscanner.py --host 192.168.1.5


Safety & Ethics

Use this tool only on networks you own or where you have explicit permission to run discovery. Unauthorized scanning of third-party networks may be illegal and unethical.

Requirements:
Python 3.8+
scapy
termcolor