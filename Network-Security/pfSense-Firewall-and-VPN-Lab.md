# pfSense Firewall, Port Forwarding, and IPSec VPN Configuration

## Objective
The objective of this lab was to configure a pfSense firewall to secure network traffic, implement port forwarding, and establish a secure site-to-site IPSec VPN tunnel between two networks.

## Lab Environment
- pfSense CE firewall (virtual machine)
- Windows 10 virtual machines
- VMware vSphere environment
- Private lab network

## Skills Demonstrated
- Firewall configuration
- Network segmentation
- NAT and port forwarding
- VPN configuration (IPSec)
- Network troubleshooting

---

## Part 1: Firewall Configuration

### Steps performed

- Installed pfSense firewall
- Configured WAN interface: 10.174.243.254/24
- Configured LAN interface: 192.168.243.1/24
- Enabled DHCP server on LAN
- Connected Windows 10 VM to LAN network
- Verified connectivity using ping

### Result

Successfully established communication between LAN host and pfSense firewall.

---

## Part 2: Port Forwarding Configuration

### Steps performed

- Created Windows machines with static IP addresses
- Enabled Remote Desktop Protocol (RDP)
- Configured NAT port forwarding rules:

External Port 3399 → Internal 192.168.243.10:3389  
External Port 3400 → Internal 192.168.243.11:3389  

- Created firewall rule to allow ICMP traffic
- Verified remote access using RDP

### Result

Successfully accessed internal machines from external network using port forwarding.

---

## Part 3: Site-to-Site IPSec VPN Configuration

### Steps performed

- Configured two pfSense firewalls
- Created IPSec Phase 1 tunnel using:

Encryption: AES-256  
Authentication: SHA256  
Authentication method: Pre-Shared Key  

- Configured Phase 2 tunnel with LAN subnets
- Created firewall rules to allow traffic
- Verified tunnel status as Established

### Result

Successfully created secure VPN tunnel allowing communication between two networks.

---

## What I Learned

This project helped me understand:

- How firewalls control network traffic
- How NAT and port forwarding work
- How VPN tunnels secure communication
- How to troubleshoot connectivity issues

---

## Tools Used

pfSense  
VMware  
Windows 10  
IPSec VPN
