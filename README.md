# subcalc

**subcalc** is a lightweight, terminal-based subnet calculator written in Bash.  
It helps you quickly calculate subnet masks from required hosts, or get full subnet details (network ID, usable IPs, broadcast, etc.) from an IP and mask.

Perfect for CCNA students, network engineers, and anyone who needs fast subnet math without leaving the terminal.

### Features

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


### Installation

1. Clone the repository:
```
git clone https://github.com/roberto1511/subcalc.git
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
Now you can run it from anywhere.

### Usage
subcalc (number of hosts)

subcalc (IP mask)

subcalc (IP/mask)

Show help:
subcalc --help
subcalc -h
subcalc help
