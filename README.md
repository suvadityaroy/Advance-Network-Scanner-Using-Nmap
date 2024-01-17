# GoScan: Advanced Network Scanner

## Overview

GoScan is an interactive network scanner client, built in Go (Golang), featuring auto-completion and providing abstraction and automation over Nmap functionalities. Originally a small side-project for learning Go, it has evolved into a powerful tool for host discovery, port scanning, and service enumeration.

## Key Features

- **Auto-completion and Abstraction:** GoScan features auto-completion, providing abstraction and automation over Nmap functionalities.
  
- **SQLite Database:** Scans maintain their state in an SQLite database, allowing asynchronous results upload even in unstable environments.

- **Service Enumeration Integration:** The Service Enumeration phase integrates various tools like EyeWitness, Hydra, and nikto, tailored for specific services.

## Installation

### Binary Installation (Recommended)

```bash
# Linux (64bit)
$ wget https://github.com/marco-lancini/goscan/releases/download/v2.4/goscan_2.4_linux_amd64.zip
$ unzip goscan_2.4_linux_amd64.zip
$ chmod +x goscan
$ sudo mv ./goscan /usr/local/bin/goscan
```

### Build from Source

```bash
$ git clone https://github.com/marco-lancini/goscan.git
$ cd goscan/
$ docker-compose up --build
$ docker-compose run cli /bin/bash
$ make init
$ make setup
$ make build
$ make cross
```

## Usage

GoScan supports various steps of network enumeration:

### 1. Load Targets

```bash
load target SINGLE <IP/32>
load target MULTI <path-to-file>
```

### 2. Host Discovery

```bash
sweep <TYPE> <TARGET>
load alive SINGLE <IP>
load alive MULTI <path-to-file>
```

### 3. Port Scanning

```bash
portscan <TYPE> <TARGET>
load portscan <path-to-file>
```

### 4. Service Enumeration

```bash
enumerate <TYPE> DRY <TARGET>
enumerate <TYPE> <POLITE/AGGRESSIVE> <TARGET>
```

### 5. Special Scans

```bash
special eyewitness  # Take screenshots (KALI ONLY)
special domain <users/hosts/servers>  # Extract Windows domain information
special dns DISCOVERY <domain>  # Enumerate DNS
special dns BRUTEFORCE <domain>  # Bruteforce DNS
special dns BRUTEFORCE_REVERSE <domain> <base_IP>  # Reverse Bruteforce DNS
```

### 6. Utils

```bash
show <targets/hosts/ports>
set config_file <PATH>  # Automatically configure settings
set output_folder <PATH>  # Change the output folder
set nmap_switches <SWEEP/TCP_FULL/TCP_STANDARD/...> <SWITCHES>  # Modify default Nmap switches
set_wordlists <FINGER_USER/FTP_USER/...> <PATH>  # Modify default wordlists
```

## External Integrations

Service Enumeration supports integrations with various tools for ARP, DNS, FINGER, FTP, HTTP, RDP, SMB, SMTP, SNMP, SSH, SQL, VNC.

---

*Combined with the "Advanced Network Scanner Using Nmap" project, GoScan significantly improves network security and efficiency. It offers a proactive approach to vulnerability identification, showcasing expertise in network security, scripting, and project management. The project's impact includes substantial improvements in network security, streamlined assessment processes, and overall contributions to the organization's success in maintaining a secure and efficient network infrastructure.*
