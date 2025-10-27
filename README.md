# Task-5-Capture-and-Analyze-Network-Traffic-Using-Wireshark

**Objective**

The objective of this task was to capture live network packets and identify basic protocols and traffic types.

**Tools Used**

1)Wireshark (free)

2)Kali Linux terminal (for generating traffic using Nmap)

3)Active network interface (to monitor and capture live packets)


**Steps I Followed**

*Installed Wireshark on my system.

*Selected the active network interface and started capturing live packets.

*Opened a few websites and pinged servers to generate traffic.

*Ran Nmap scans while Wireshark was capturing.

*Stopped the capture after about one minute.

*Used Wireshark filters to analyze specific traffic types.

*Identified at least three different protocols in the capture.

*Saved the packet capture file as network_traffic.pcap.


**Nmap Commands Used**


1)TCP SYN scan (subnet)

sudo nmap -sS

Used to perform a half-open TCP SYN scan to find open ports efficiently.


2)Full TCP port scan (all ports)

sudo nmap -sS -p- -T4

Scans all 65,535 TCP ports on a host quickly to detect active services.


3)UDP top 50 ports scan

sudo nmap -sU --top-ports 50

Checks the top 50 most common UDP ports to identify UDP-based services.


**Filters Used in Wireshark**

##SYN packets (scan probes): tcp.flags.syn==1 && tcp.flags.ack==0

##SYN-ACK packets (open port replies): tcp.flags.syn==1 && tcp.flags.ack==1

##RST packets (closed ports): tcp.flags.rst==1

##ARP packets: arp


**Protocols Identified**

In the captured packets, I identified the following network protocols:


1)ARP – Address Resolution Protocol (IP to MAC address mapping)

2)DNS – Domain Name System (domain name resolution)

3)TCP – Transmission Control Protocol (connection establishment and communication)

4)UDP – Connectionless communication used for services like DNS

5)ICMP – Used for ping requests and responses


**Findings**

*Wireshark successfully captured all packets generated during browsing and scanning.

*TCP SYN, SYN-ACK, and RST packets confirmed scanning activity.

*ARP packets helped identify device IP and MAC address mappings.

*DNS packets showed the domain name lookups from web browsing.

*ICMP packets showed ping request and reply sequences.


**Example Findings**

**Field	Example Data**

Total Packets Captured-----------3200

Capture Duration-----------------1 minute

Source IP (Scanner)--------------192.xxx.x.xx

Destination IP-------------------192.xxx.x.x

Observed Protocols---------------ARP, DNS, TCP, UDP, ICMP


**Sample Packet Evidence**

1)SYN Packet: Source 192.xxx.x.xx → Dest 192.xxx.x.x, Flags: SYN

2)SYN-ACK Packet: Source 192.xxx.x.x → Dest 192.xxx.x.xx, Flags: SYN, ACK

3)RST Packet: Source 192.xxx.x.x → Dest 192.xxx.x.xx, Flags: RST


**Export**

After the capture and analysis were completed:

1)Went to File → Save As in Wireshark.

2)Saved the capture file as network_traffic.pcap.

3)Uploaded this file with the README to the repository.

4)Summary of Findings (like findings.txt)

5)Task 5: Wireshark Network Traffic Analysis


**Objective:**


To capture and analyze live network traffic and identify common network protocols.

Protocols Found:

ARP – Address Resolution Protocol

DNS – Domain Name System

TCP – Transmission Control Protocol

UDP – User Datagram Protocol

ICMP – Internet Control Message Protocol


**Summary of Findings:**

##Captured TCP SYN, SYN-ACK, and RST packets during Nmap scans.


##ARP packets mapped IP addresses to MAC addresses.


##DNS queries and responses were visible when visiting websites.


##ICMP packets showed ping request and reply activity.


##Network communication between devices was successfully analyzed.


**Capture File:**

Saved as network_traffic.pcap


**Key Learnings**


1)Learned how to identify different protocols in real-time.


2)Understood how scanning activity appears in Wireshark.


3)Learned to use filters and analyze packets effectively.


Gained knowledge about TCP handshakes, ARP mapping, and DNS resolution.



**Outcome**

By completing this task, I gained hands-on experience in--- Capturing and analyzing live network traffic,  Using Wireshark filters for specific protocols,  Understanding how TCP, UDP, ARP, and DNS traffic behaves.

Recognizing how scanning and normal communication appear in packet captures.

Conclusion

This task helped me develop packet analysis skills and protocol awareness.
I successfully captured live network traffic, analyzed scan patterns, and identified multiple network protocols using Wireshark.
