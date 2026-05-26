# Networking basics #1
## What is localhost / 127.0.0.1?

Hostname that refers to the current computer.

127.0.0.1 is the IPv4 loopback address that points back to the current machine.

They are used to allow a computer to communicate with itself for testing or development.

A web server running can be accessed at http://localhost

This is equivalent to http://127.0.0.1

## What is 0.0.0.0?

0.0.0.0 is a special IP address that means “all IPv4 addresses on the local machine”.

It is commonly used to:

- Bind a service to all network interfaces
- Make a server accessible from other devices on the network


A server listening on 0.0.0.0:8080 means it accepts connections from any network interface (not just localhost).
## What is /etc/hosts?

Local system file used to map hostnames to IP addresses.

It is checked before DNS when resolving domain names.

Example content:
```
127.0.0.1   localhost
192.168.1.10 myserver.local
```

Uses:

- Override DNS locally
- Test domains without changing DNS settings
- Define local machine name mappings
## How to display your machine's active network interfaces
### On Linux / macOS:
```
ifconfig
```
or
```
ip a
```

### On Windows:
```
ipconfig
```
### What it shows:
- Network interface names (eth0, wlan0, etc.)
- IP addresses
- MAC addresses
- Connection status
