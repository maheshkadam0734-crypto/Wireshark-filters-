Wireshark Filters – A Practical Guide

Activity: Computer Networks – Wireshark Filter Demonstration
Domain: Computer Networking and Network Security
Tool Used: Wireshark Network Protocol Analyzer

---

1. Introduction

Wireshark is an open-source network protocol analyzer used to capture, monitor, and analyze network traffic in real time. It helps network administrators, cybersecurity professionals, and students understand how data travels across a network.

Wireshark provides filtering capabilities that allow users to identify specific network packets based on protocols, IP addresses, port numbers, and other parameters.

2. Objective

- To understand the working of Wireshark filters.
- To identify different network protocols.
- To analyze network traffic based on IP addresses and port numbers.
- To monitor specific types of network communication.
- To develop practical knowledge of network troubleshooting and security analysis.

3. Types of Wireshark Filters

Wireshark provides two major types of filters:

3.1 Capture Filters

Capture filters are used to specify which packets should be captured during network monitoring.

Examples:

Filter| Description
"host 192.168.1.10"| Captures traffic to or from a specific IP address.
"src host 192.168.1.10"| Captures packets from a specific source IP.
"dst host 192.168.1.10"| Captures packets destined for a specific IP.
"port 80"| Captures traffic using port 80.
"tcp"| Captures TCP packets.
"udp"| Captures UDP packets.
"icmp"| Captures ICMP packets.
"net 192.168.1.0/24"| Captures traffic belonging to a specific network.

3.2 Display Filters

Display filters are used to filter packets that have already been captured. They help users focus on specific network traffic without deleting other captured packets.

4. Common Wireshark Display Filters

4.1 Protocol-Based Filters

Filter| Description
"tcp"| Displays TCP packets.
"udp"| Displays UDP packets.
"icmp"| Displays ICMP packets.
"arp"| Displays ARP packets.
"dns"| Displays DNS traffic.
"http"| Displays HTTP packets.
"https"| Displays HTTPS/TLS-related traffic.
"dhcp"| Displays DHCP packets.
"ftp"| Displays FTP traffic.
"ssh"| Displays SSH traffic.

4.2 IP Address-Based Filters

Filter| Description
"ip.addr == 192.168.1.10"| Displays packets involving a specific IP address.
"ip.src == 192.168.1.10"| Displays packets from a specific source IP.
"ip.dst == 192.168.1.10"| Displays packets sent to a specific destination IP.
"ip.src == 192.168.1.1 && ip.dst == 192.168.1.10"| Displays traffic between two specified IP addresses in one direction.
"ip"| Displays IPv4 packets.
"ipv6"| Displays IPv6 packets.

4.3 Port-Based Filters

Filter| Description
"tcp.port == 80"| Displays TCP traffic using port 80.
"tcp.port == 443"| Displays TCP traffic using port 443.
"tcp.port == 22"| Displays SSH-related TCP traffic.
"udp.port == 53"| Displays UDP traffic using DNS port 53.
"tcp.srcport == 80"| Displays packets originating from TCP port 80.
"tcp.dstport == 443"| Displays packets destined for TCP port 443.

4.4 TCP Analysis Filters

Filter| Description
"tcp.flags.syn == 1"| Displays TCP packets with the SYN flag set.
"tcp.flags.ack == 1"| Displays TCP packets with the ACK flag set.
"tcp.flags.fin == 1"| Displays TCP packets with the FIN flag set.
"tcp.flags.reset == 1"| Displays TCP packets with the RST flag set.
"tcp.analysis.retransmission"| Identifies TCP retransmissions.
"tcp.analysis.duplicate_ack"| Identifies duplicate TCP acknowledgements.
"tcp.analysis.lost_segment"| Identifies packets indicating a possible lost TCP segment.

4.5 DNS and HTTP Filters

Filter| Description
"dns"| Displays DNS queries and responses.
"dns.flags.response == 0"| Displays DNS queries.
"dns.flags.response == 1"| Displays DNS responses.
"http.request"| Displays HTTP requests.
"http.response"| Displays HTTP responses.
"http.request.method == "GET""| Displays HTTP GET requests.
"http.request.method == "POST""| Displays HTTP POST requests.

4.6 Logical Operator Filters

Operator| Description
"&&"| AND – Both conditions must be true.
`| 
"!"| NOT – Excludes a particular condition.
"=="| Checks equality.
"!="| Checks inequality.
">"| Greater than.
"<"| Less than.

Examples:

- "tcp && ip" – Displays IPv4 TCP packets.
- "tcp || udp" – Displays TCP or UDP packets.
- "!arp" – Excludes ARP packets.
- "tcp.port == 80 && ip" – Displays IPv4 TCP traffic involving port 80.

5. Practical Applications

Wireshark filters are useful in several networking and cybersecurity activities:

1. Network Troubleshooting: Identifying connectivity issues and packet retransmissions.
2. Protocol Analysis: Understanding how protocols such as TCP, UDP, DNS, and HTTP work.
3. Security Monitoring: Observing unusual or unexpected network communication.
4. Traffic Analysis: Identifying communication between different devices.
5. Performance Analysis: Investigating packet loss, duplicate acknowledgements, and retransmissions.

6. Procedure to Apply Filters in Wireshark

1. Open the Wireshark application.
2. Select an available network interface.
3. Start capturing network packets.
4. Generate network traffic by browsing websites or using network commands.
5. Enter the required filter in the Display Filter bar.
6. Press Enter to apply the filter.
7. Observe the filtered packets and analyze their details.
8. Stop the packet capture after completing the activity.

7. Result

The practical activity demonstrates how Wireshark filters can be used to capture, identify, and analyze specific network traffic. Different filters help isolate protocols, IP addresses, port numbers, and TCP communication patterns, making network monitoring and troubleshooting easier.

8. Conclusion

Wireshark is an important tool for understanding computer networks and network security. By using capture and display filters, users can efficiently analyze network communication and identify specific packets. This activity provides practical knowledge of packet analysis and builds a foundation for advanced networking and cybersecurity concepts.

---

References:

- Wireshark Official Website: https://www.wireshark.org/
- Wireshark Display Filter Reference: https://www.wireshark.org/docs/dfref/
- Wireshark User's Guide: https://www.wireshark.org/docs/wsug_html_chunked/

Note: Capture filters and display filters use different syntax. The examples in this report are intended for educational and authorized network analysis.# Wireshark-filters-
 A practical guide to Wireshark filters for computer networking and cybersecurity.
