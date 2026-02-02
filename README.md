# Task 9: Network Vulnerability Scanning

## Objective
To scan a local network, identify open ports, detect services, analyze vulnerabilities, and document findings using Nmap.

## Tools Used
- Nmap
- Masscan (Alternative)

## Steps Performed

### 1. Scan Local Network
```
nmap -sn 192.168.1.0/24
```

### 2. Identify Open Ports
```
nmap 192.168.1.1
```

### 3. Detect Services
```
nmap -sV 192.168.1.1
```

### 4. Identify Operating System
```
nmap -O 192.168.1.1
```

### 5. Vulnerability Scanning
```
nmap --script vuln 192.168.1.1
```

### 6. Save Scan Results
```
nmap -sV -O 192.168.1.1 -oN scan_report.txt
```

## Findings
| Port | Service | Risk |
|------|---------|------|
| 21 | FTP | Anonymous login risk |
| 22 | SSH | Brute force attack |
| 80 | HTTP | Web vulnerabilities |
| 445 | SMB | EternalBlue exploit risk |

## Recommendations
- Close unused ports
- Update outdated services
- Use firewall rules
- Apply strong passwords

## Conclusion
Network vulnerability scanning helps identify security weaknesses and improves defensive security posture.

Prepared by: SAFFIQ MOHAMMED S
