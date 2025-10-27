# Networking + OS Cybersecurity Practice

Hands-on, OS-focused cybersecurity labs spanning Linux and Windows. Learn how networks and operating systems interact, capture and analyze traffic, map sockets to processes, harden hosts, respond to incidents, and build small tools that prove your skills.

## Who this is for
- Students and engineers building practical networking + OS security skills
- Interview prep or portfolio builders
- Anyone who prefers "learn-by-doing" on real systems

## What you’ll learn
- Network fundamentals (interfaces, routes, TCP states)
- Packet capture and protocol analysis
- Socket programming (write a tiny TCP server/client)
- Host firewalls (Linux nftables/ufw; Windows Defender Firewall)
- Mapping processes to connections (procfs, IP Helper API concepts)
- DNS security basics (DoH vs DoT, cache, integrity)
- Incident response triage (network + process evidence)
- Intro to IDS (Zeek/Suricata) and container networking
- CI/CD hygiene for security projects

## Labs
| # | Lab | OS | Est. time |
|---|-----|----|-----------|
| 00 | Lab Safety & Ethics | Both | 10m |
| 01 | Network Fundamentals | Both | 45m |
| 02 | Packet Capture & Analysis | Both | 60m |
| 03 | Socket Programming | Both | 60m |
| 04 | Host Firewalling | Both | 60m |
| 05 | Process ↔ Socket Mapping | Linux-first | 90m |
| 06 | Incident Response Triage | Both | 60m |
| 07 | DNS Security Basics | Both | 45m |
| 08 | IDS Intro (Zeek) | Linux | 90m |
| 09 | Container Networking | Linux | 75m |
| 10 | CI/CD Security (GitHub) | N/A | 45m |

Start with SETUP.md, then follow labs in order.

## Quick start
- Read SETUP.md to create a safe lab (VMs or containers)
- Do labs 00 → 05 to cover core OS + networking
- Use docs/cheatsheets for quick command references

## Safety
All labs are designed for a private lab environment. Never target networks/systems without explicit authorization. See SECURITY.md.
