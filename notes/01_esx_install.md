# ESX Installation

## ESX 1

- Select a Disk to Install: `NVMe SSD 970 EVO Plus 500GB`
- Keyboard Layout: `Swiss French`
- Set root password

---

- Configure Management Network
  - IPv4 Configuration
    - IP Address: `192.168.1.10`
    - Subnet Mask: `255.255.255.0`
    - Default Gateway: `192.168.1.1`
  - DNS Configuration
    - Primary DNS: `62.2.24.162`
    - Alternate DNS: `62.2.17.60`
    - Hostname: `esx01`
  - Custom DNS Suffixes: `v.cablecom.net`

## ESX 2

- Select a Disk to Install: `NVMe SSD 970 EVO Plus 500GB`
- Keyboard Layout: `Swiss French`
- Set root password

---

- Configure Management Network
  - IPv4 Configuration
    - IP Address: `192.168.1.11`
    - Subnet Mask: `255.255.255.0`
    - Default Gateway: `192.168.1.1`
  - DNS Configuration
    - Primary DNS: `62.2.24.162`
    - Alternate DNS: `62.2.17.60`
    - Hostname: `esx02`
  - Custom DNS Suffixes: `v.cablecom.net`
