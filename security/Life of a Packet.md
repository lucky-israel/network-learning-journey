A network engineer sees packets as units of data to be forwarded. A security engineer sees packets as potential lies that need to be checked:

* Is the source IP truthful, or is it spoofed?

* Is this TCP connection legitimate, or part of a DoS attack?

* Is this ARP reply from the real owner of the IP?

* Should this port/VLAN even be sending this type of traffic?

Projects : Implement a defense. On your router or switch, create an ACL that blocks ICMP from unauthorized subnets.


OSI Layer	Network Engineer Questions (The "How")	Security Engineer Questions (The "What If")
1. Application	What service is being requested (HTTP, DNS, SSH)? What's the destination port?	Is this traffic allowed by policy? Is this web request hiding malicious code? Is this DNS query going to a malicious domain?
2. Transport (TCP/UDP)	Is it TCP (reliable, connection-oriented) or UDP (fast, connectionless)? What's the source port? For TCP, what's the state of the handshake?	Can I see SYN floods (DoS attack)? Are there unusual TCP flags (Xmas tree scan)? Is a high-numbered source port trying to talk to a service port (malware beaconing)?
3. Network (IP)	What's the source and destination IP? What's the TTL? What route will it take based on the routing table?	Is the source IP spoofed? Is this an IP from an unauthorized subnet? Is the TTL unusually low (traceroute evasion)?
4. Data Link (MAC)	What's the destination MAC address? Is it the switch's MAC, a router's MAC, or another host's MAC? What VLAN is it on?	Is this an ARP poisoning attempt (is the IP-MAC pair correct)? Is this a MAC flooding attack (too many MACs on a port)? Is this VLAN hopping traffic?
5. Physical	Is the link up? Are there errors on the interface?	Has the cable been tampered with? Is there a unauthorized device connected (check port security)?
