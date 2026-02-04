# subcalc

**subcalc** is a lightweight, terminal-based subnet calculator written in Bash.  
It helps you quickly calculate subnet masks from required hosts, or get full subnet details (network ID, usable IPs, broadcast, etc.) from an IP and mask.

Perfect for CCNA students, network engineers, and anyone who needs fast subnet math without leaving the terminal.

## Features

- Calculate optimal subnet mask (/CIDR, decimal, binary, hex) from number of required hosts
- Compute full subnet information: network address, first/last usable IP, broadcast, usable hosts count
- Supports multiple input formats:
  - Decimal IP (192.168.1.1)
  - CIDR notation (10.1.2.3/26)
  - Binary (with or without dots)
  - Hex (with or without dots)
- Random private network example when calculating from hosts
- Colorful, readable output
- Zero external dependencies (pure Bash)


## Installation

1. Clone the repository:
```
bash
git clone https://github.com/YOUR_USERNAME/subcalc.git
cd subcalc
```

2. Make the script executable:
```
sudo chmod +x subcalc
```

3. (Optional) Move it to a directory in your PATH for global access:
```
sudo mv subcalc /usr/local/bin/
```
Now you can run it from anywhere:

```
subcalc 28
```

## Usage
subcalc <number of hosts>
subcalc <IP> <mask>
subcalc <IP/mask>

## Examples
# Calculate mask for 120 hosts
subcalc 120

# Full subnet details
subcalc 192.168.10.45 /27

subcalc 10.1.2.3 255.255.255.192

subcalc 172.16.5.100 255.255.252.0

# CIDR shorthand
subcalc 192.168.1.50/26

# Binary and hex inputs
subcalc 11000000101010000000101000110010 /27
subcalc C0A80A32 FFFFFFE0

## Show help:
subcalc --help
subcalc -h
subcalc help

## Output Example
Calculation for 120 requested hosts:
-----------------------------------
Usable hosts        : 126
Host bits           : 7
CIDR prefix         : /25
Decimal mask        : 255.255.255.128
Binary mask         : 11111111.11111111.11111111.10000000
Hex mask            : FF.FF.FF.80
-----------------------------------
Usage example: subcalc 10.145.78.0 /25
