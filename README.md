<div align="center">

# 🔍 Advance Network Scanner Using Nmap

<img src="https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS%20%7C%20Raspberry%20Pi-blue" />
<img src="https://img.shields.io/badge/Go-1.21%2B-00ADD8" />
<img src="https://img.shields.io/badge/Nmap-7.80%2B-2a62ff" />
<img src="https://img.shields.io/badge/Status-Active-brightgreen" />

<br/>

<pre>
╔══════════════════════════════════════════════════════════════════════╗
║                         ADVANCE NETWORK SCANNER                      ║
╚══════════════════════════════════════════════════════════════════════╝
   ⚡ Cross-Platform • 🎛️ Menu-Driven • 🧠 Powered by Nmap
</pre>

</div>


## 🧭 What It Is

Advance Network Scanner is a professional, menu-driven network reconnaissance toolkit. It wraps Nmap with a polished CLI, smart defaults, colorful output, and optional result caching—ideal for security engineers, sysadmins, and learners.

Supported: Windows • Linux (Kali/Ubuntu) • macOS • Raspberry Pi 5

---

## ✨ Features

- 🎛️ Organized scan catalog (Basic, Security, Discovery, TCP, ARP, Web, Auth, IoT, etc.)
- 🌐 Cross-platform binaries and Docker support
- 🧠 Nmap integration with safe/aggressive presets
- 🎨 Colorized, animated CLI for smoother UX
- 💾 Optional SQLite caching (Linux/macOS)
- 🔍 Service fingerprinting and enumeration modules
- 🧩 Extensible design with utilities and helpers

Supported protocols/services: ARP, DNS, ICMP, TCP, UDP, SSH, FTP, SMTP, HTTP(S), RDP, SMB, SNMP, SQL, VNC, LDAP.

---

## 🧱 Tech Stack & Languages

- Go (Golang) 1.21+
- Nmap 7.80+
- SQLite (non-Windows builds)
- ANSI-color CLI (Fatih Color)

Design: goroutines for concurrency, structured logging, INI-style configuration, modular `core/` with `cli/`, `scan/`, `enum/`, `model/`, `utils/`.

---

## 📦 Install

### Windows
```powershell
# Install prerequisites
choco install golang
choco install nmap

# Clone and build
git clone https://github.com/suvadityaroy/Advance-Network-Scanner-Using-Nmap.git
cd Advance-Network-Scanner-Using-Nmap\goscan
$env:CGO_ENABLED = '0'
go build -o goscan.exe main.go

# Run as Administrator
./goscan.exe
```

### Linux (Kali/Ubuntu)
```bash
sudo apt update && sudo apt install -y golang-go nmap git
git clone https://github.com/suvadityaroy/Advance-Network-Scanner-Using-Nmap.git
cd Advance-Network-Scanner-Using-Nmap/goscan
make build   # or: make build-kali / make build-rpi
sudo ./goscan
```

### macOS
```bash
brew install go nmap
git clone https://github.com/suvadityaroy/Advance-Network-Scanner-Using-Nmap.git
cd Advance-Network-Scanner-Using-Nmap/goscan
go build -o goscan main.go
sudo ./goscan
```

### Docker (optional)
```bash
docker compose up --build
```

---

## 🚀 Usage

```bash
# Linux/macOS/Raspberry Pi
sudo ./goscan

# Windows (Administrator)
./goscan.exe
```

Animated menu example:

```
╔══════════════════════════════════════════════════════════════════╗
║                      🔍 ADVANCE SCANNER MENU                     ║
╚══════════════════════════════════════════════════════════════════╝
 1) Basic Scans      2) Security Scans     3) Network Discovery
 4) TCP Scans        5) ARP Scans          6) Authentication
 7) Web Scans        8) See More           9) View Logs
10) View Cache      11) Exit
▶ Enter your choice (0-11):
```

---

## 🔧 Configuration

Paths:
- Linux/macOS: `~/.goscan/config.cfg`
- Windows: `%USERPROFILE%\.goscan\config.cfg`

Example:
```ini
[nmap]
default_switches = -sV
default_timing = T3
max_retries = 2

[output]
color_enabled = true
verbose = true
```

---

## 🗂️ Project Layout

```
Advance-Network-Scanner-Using-Nmap/
├── README.md
├── CHANGELOG.md
├── docker-compose.yml
├── goscan/
│   ├── main.go
│   ├── core/
│   │   ├── cli/
│   │   ├── scan/
│   │   ├── enum/
│   │   ├── model/
│   │   └── utils/
│   └── sample_config.cfg
└── cli/
```

---

## 🛡️ Legal

⚠️ Use only on networks you own or have explicit written permission to assess.

---

## 🧰 Troubleshooting

- Run as Administrator (Windows) or with `sudo` (Linux/macOS)
- If `nmap` is missing: install via package manager or https://nmap.org/download.html
- Rebuild: `make clean && make build`

---

## 👨‍💻 Created By

**Suvaditya Roy**

<div align="center">

<pre>
✨ Thank you for using Advance Network Scanner! ✨
</pre>

</div>
