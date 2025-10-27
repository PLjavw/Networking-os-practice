# Lab 01: Network Fundamentals

Objectives
- Inspect interfaces and routes
- Observe TCP states
- Verify connectivity within your lab

Linux
```bash
ip a
ip route
ping -c 3 8.8.8.8
ss -tuna | head
ss -tulpen | head  # needs sudo to show PIDs
