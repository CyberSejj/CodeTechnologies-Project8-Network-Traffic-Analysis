Project 8: Network Traffic Analysis

Organization: Code Technologies
Tools Used: Kali Linux, Oracle VirtualBox, Wireshark
Wireshark Version: 4.6.6

1. Introduction

Network traffic analysis is the process of examining network packets to understand communication between devices. This project involved using Wireshark in Kali Linux to observe network traffic and perform basic connectivity, DNS, and HTTP response checks.

2. Objectives

- Identify available network interfaces and IP addresses.
- Capture and examine network packets using Wireshark.
- Observe ICMP traffic and understand packet loss.
- Analyze DNS queries and responses.
- Verify an HTTP server response.

3. Tools and Environment

- Kali Linux running in Oracle VirtualBox
- Wireshark 4.6.6
- "ip -br addr"
- "ping"
- "nslookup"
- "curl"

4. Practical Work and Observations

4.1 Network Interface Identification

The following interfaces were identified:

Interface| IP Address
eth0| 10.0.2.15
eth1| 192.168.56.101
lo| Loopback interface

4.2 Connectivity Testing

A ping test to "1.1.1.1" completed successfully. Four packets were transmitted and four were received, resulting in 0% packet loss.

A separate ping test to "192.168.56.1" resulted in 100% packet loss. No successful replies were received during that test.

4.3 ICMP Traffic Analysis

Wireshark captured traffic on "eth1". Using the "icmp" display filter, four ICMP Echo Requests were observed from "192.168.56.101" to "192.168.56.1".

The observed requests did not establish successful connectivity to the destination.

4.4 DNS Analysis

The command "nslookup example.com" successfully returned IPv4 and IPv6 addresses using DNS server "10.0.2.3".

Wireshark was also used on "eth0" to observe DNS queries and responses.

4.5 HTTP Response Verification

The command "curl -I http://example.com" returned the status "HTTP/1.1 200 OK".

This confirmed that an HTTP response was received. It does not independently confirm that HTTP packets were captured in Wireshark.

5. Learning Outcomes

Through this project, I gained practical experience in:

- Identifying network interfaces and IP addresses.
- Understanding ICMP Echo Requests and packet loss.
- Observing DNS queries and responses.
- Checking HTTP response status codes.
- Using Wireshark display filters for packet analysis.

6. Conclusion

This project provided hands-on experience with basic network traffic analysis in Kali Linux using Wireshark. The practical exercises helped me understand network communication, DNS resolution, ICMP traffic, and HTTP response verification.

7. Evidence and Limitations

Screenshots will be included as supporting evidence. The Wireshark capture file will be added if a saved capture is located or recovered from the existing Wireshark session.

No vulnerability discovery or malicious activity was claimed as part of this project.
