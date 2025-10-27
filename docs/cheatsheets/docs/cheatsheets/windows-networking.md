# Windows Networking Cheatsheet

Interfaces and routes
- Interfaces: `Get-NetAdapter`
- IP config: `Get-NetIPAddress`
- Routes: `route print` or `Get-NetRoute`

Sockets and services
- TCP connections: `Get-NetTCPConnection`
- Listening: `Get-NetTCPConnection -State Listen`
- Map PIDs: `netstat -ano`; map with `Get-Process -Id <PID>`

Packet capture
- Install Npcap; capture in Wireshark
- PowerShell ETW trace (advanced): `New-NetEventSession`, `Add-NetEventPacketCaptureProvider`

Name resolution
- DNS lookup: `Resolve-DnsName example.com`
- Hosts file: `C:\Windows\System32\drivers\etc\hosts`

Firewall
- Allow 8080 (inbound): `New-NetFirewallRule -DisplayName "Allow 8080 TCP" -Direction Inbound -Protocol TCP -LocalPort 8080 -Action Allow`
- Show rules: `Get-NetFirewallRule | ? DisplayName -like "*8080*"`

Misc
- Test port: `Test-NetConnection -ComputerName 127.0.0.1 -Port 8080`
- Traceroute: `tracert 8.8.8.8`
