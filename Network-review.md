## Networking

- dotted quad (format of IPv4 address):  4-bytes.4-bytes.4-bytes.4-bytes; 32-bits
- host: devices on a network
- subnet:  sub-network;  ISP Sub-nets to Customers; Customers sub-nets into private/home network
  - Network prefix:  Class A, B, C, D; ISP owns 192.0.0.0 vs 192.168.0.0 vs 192.168.1.0
  - Subnet mask:  255.255.255.255
  - CIDR notation (substitute for long form subnet mask)   255.255.255.0/8
- gateway: a node (router) in a computer network, a key stopping point for data on its way to or from other networks.
- Default Gateway - bounded IP data sent to when outside network
- routing
  - Read a routing table for where traffic will be routed
    * Destination 10.0.0.x with netmask 255.255.255.0 will talk to all devices on 10.0.0.x network
  - MAC addresses:  Media Access Control/Manufacturer based ID 
  - arp table associates MAC with IP
- Hardware interface names (common)
  - eth0, wifi0 / wlan0, lo
- DNS:  www.google.com vs 8.8.8.8
  - Local hostname resolution
    - Role of /etc/hosts: a static lookup method/mapping for resolution, locally used in sys admin purposes
    - Role of /etc/resolv.conf:  lists nameservers that are used by your host for DNS resolution. 
- Ports (common)
  - 22 (SSH), 80 (HTTP), 443 (HTTPS)
  - Read output of netstat with flags (-n -t -l)
- What an IP address tells you about the network:
  - Private network prefixes:
    - 10.0.0.0/8
    - 192.168.0.0/16
    - 172.16.0.0/12
  - Local network prefixes:
    - 127.0.0.0/8
- Router (as separate hardware):
  - NAT:  Network Address Translation:  Private to Public translation
  - DHCP:   Dynamic Host Configuration Protocol:  assigns IP addresses to hosts in a private network
- Firewall
  - INPUT, OUTPUT, FORWARD chains
  - Can be managed at router level or host level
  - Host level management in Linux: iptables
  - Packet is blocked by first rule that matches in chain
- Forward proxy vs VPN
- Reverse proxies:
  - Caching
  - Load balancing (web servers):  Round Robin, Weighted Round Robin, Least Connections, Least Response Time
    * Round Robin:  Prioritize First In to Bottom of List, looping
    * Weighted Round Robin:  Factoring in X where X can be other connections still in load balancer, etc etc
    * Least Connections:  Systems who have lowest connections are priority
    * Least Response Time:  Systems who have faster response time are priority
    - Monitor services?
    - Allocation strategies
    - Connection maintainence
    - Session persistence
