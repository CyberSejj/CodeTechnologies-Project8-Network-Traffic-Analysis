Code Technologies — Project 8: Network Traffic Analysis

Project Overview

This project focuses on capturing and analyzing network traffic using Wireshark in Kali Linux. The practical work involved examining ICMP traffic, observing DNS queries and responses, and verifying an HTTP server response.

Objectives

- Understand basic network traffic analysis.
- Capture and examine packets using Wireshark.
- Identify ICMP and DNS traffic.
- Verify an HTTP response.
- Understand how packet analysis supports network troubleshooting and security monitoring.

Tools and Environment

- Operating System: Kali Linux
- Virtualization: Oracle VirtualBox
- Network Analysis Tool: Wireshark 4.6.6
- Supporting Commands: "ip -br addr", "ping", "nslookup", "curl"

Practical Work and Results

1. Network Interface Identification

The interfaces identified included:

- "eth0" — "10.0.2.15"
- "eth1" — "192.168.56.101"
- "lo" — loopback interface

2. Connectivity Test

A ping test to "1.1.1.1" completed successfully, with 4 packets transmitted, 4 received, and 0% packet loss.

A separate ping to "192.168.56.1" showed 100% packet loss. No successful ICMP replies were observed in that test.

3. ICMP Traffic Analysis

Wireshark was used to capture traffic on "eth1". Applying the "icmp" display filter showed four ICMP Echo Requests from "192.168.56.101" to "192.168.56.1".

4. DNS Analysis

The "nslookup example.com" command successfully returned IPv4 and IPv6 addresses through DNS server "10.0.2.3". DNS queries and responses were also observed in Wireshark on "eth0".

5. HTTP Response Verification

The command "curl -I http://example.com" returned "HTTP/1.1 200 OK". This verified that an HTTP response was received. This result alone does not establish that the HTTP packets were captured in Wireshark.

Key Learning Outcomes

- Identifying network interfaces and IP addresses.
- Understanding ICMP Echo Requests and packet loss.
- Observing DNS queries and responses.
- Verifying HTTP server responses.
- Using Wireshark display filters to inspect network traffic.

Evidence

Screenshots and any saved Wireshark capture files will be added to this repository after they have been organized and verified.

Conclusion

This project provided practical experience with basic network traffic analysis using Wireshark in Kali Linux. The exercises demonstrated how to inspect network packets, observe DNS activity, and verify connectivity and HTTP responses.

Disclaimer

All testing was conducted in my own lab environment for educational purposes.