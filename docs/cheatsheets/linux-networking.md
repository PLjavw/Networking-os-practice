# Linux Networking Cheatsheet

Interfaces and routes
- Show interfaces: `ip a`
- Show routes: `ip route`
- Add route (example): `sudo ip route add 10.10.0.0/24 via 192.168.56.1`

Sockets and services
- List connections: `ss -tuna` (TCP/UDP, numeric)
- Listening services: `ss -tulpen` (show PIDs; needs sudo)
- Process tree: `ps -eo pid,ppid,cmd --forest`

Packet capture
- Quick capture: `sudo tcpdump -i any -c 20`
- Capture HTTP on loopback: `sudo tcpdump -i lo port 8000 -w http.pcap`

Name resolution
- Query: `dig A example.com @1.1.1.1`
- Hosts file: `/etc/hosts`
- Resolvers: `/etc/resolv.conf` (or systemd-resolved links)

Firewall (nftables/ufw)
- NF tables list: `sudo nft list ruleset`
- Allow 8080 (ufw): `sudo ufw allow 8080/tcp`
- Deny all inbound (ufw): `sudo ufw default deny incoming`

Misc
- Who is listening on a port: `sudo lsof -i :8080`
- Trace route: `traceroute 8.8.8.8` (install `inetutils-traceroute` if needed)
