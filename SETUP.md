# Setup

Goal: create a safe, isolated lab with a Linux VM and a Windows VM (or equivalents) plus essential tools.

## Options
1) Virtual machines (recommended)
- Hypervisor: VirtualBox, VMware Workstation, or Hyper-V
- VMs:
  - Ubuntu Server LTS (2 vCPU, 4 GB RAM)
  - Windows 11 (2 vCPU, 6 GB RAM)
- Networking:
  - NAT (internet access for updates)
  - Host-only/Private network (VM↔host, VM↔VM)

2) Single-host + containers (Linux)
- Use Docker/Podman networks for container-based labs
- Install tools on the host for packet capture and firewall labs

3) WSL2 + Windows
- Linux tools via WSL2; Windows-native tools on the host
- Note: WSL2 networking differs from full VM bridging

## Install tools

Linux (Ubuntu)
```bash
sudo apt update
sudo apt install -y wireshark tcpdump nmap nftables ufw iproute2 iputils-ping \
  netcat-openbsd curl jq net-tools htop whois dnsutils python3 python3-pip
# Optional: Zeek, Suricata via package or container later



Allow non-root capture (optional): add your user to the wireshark group and re-login.

Windows

Install: Wireshark (with Npcap), Windows Terminal, Sysinternals Suite (Sysmon optional)
PowerShell modules: Install-Module -Name PSWindowsUpdate -Scope CurrentUser (optional)
Ensure “Windows Defender Firewall” is enabled
Containers (optional)

Bash

# Docker or Podman
sudo apt install -y docker.io || sudo dnf install -y podman
# Verify
docker run --rm hello-world
Test checklist
Linux: ip a, ip route, ss -tuna, sudo tcpdump -i any -c 5
Windows: Get-NetAdapter, Get-NetRoute, Get-NetTCPConnection, Wireshark loopback capture
Both VMs can ping each other on the host-only network

