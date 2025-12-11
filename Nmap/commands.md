###############################################################################################
# This file is created by Mohamed Lebbie as part of the practical lab assignment              #
#                                                                                             #
###############################################################################################

# Nmap Commands Documentation

This file lists all Nmap commands used during the practical lab exercises, along with a brief explanation of each command.

---

# Host Discovery
```bash
# Ping scan to discover live hosts in the subnet
nmap -sN 10.6.6.0/24

# Performs a ping sweep on the entire 10.6.6.0/24 network to identify live hosts without scanning ports.
nmap -sn 10.6.6.0/24
```

# Port Scanning
```bash
# TCP SYN scan on all ports
nmap -sS -p- 10.6.6.23

# TCP connect scan on common ports
nmap -sT 10.6.6.23

# UDP scan on ports 1-100
nmap -sU -p 1-100 10.6.6.23
```

# Service and Version Detection
```bash
# Detect services and their versions
nmap -sV 10.6.6.23
```

# OS Fingerprinting
```bash
# Detect the operating system of the target host
nmap -O 10.6.6.23
```
# Nmap Scripting Engine (NSE)
```bash
# Run NSE script to check for anonymous FTP access
nmap --script ftp-anon 10.0.0.15

# Check HTTP title of the web server
nmap --script http-title 10.6.6.23

# Get SSH host keys
nmap --script ssh-hostkey 10.6.6.23

# Enumerates SMB shares on the target, showing shared folders, permissions, and anonymous access status.
nmap --script smb-enum-shares.nse -p445 10.6.6.23
```

# Aggressive Scan
```bash
# Aggressive scan with OS detection, version detection, script scanning, and traceroute
nmap -A 10.6.6.23

# Aggressive scan on port 21 with OS detection, version detection, script scanning, and traceroute
nmap -p21 -sV -A -T4 10.6.6.23

# Aggressive scan on SMB ports 139 and 445 to detect OS, services, versions, and run default scripts.
nmap -A -p139,445 10.6.6.23
