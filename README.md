# Nmap and Scapy Practical Lab Documentation

This repository presents a comprehensive documentation of my practical laboratory work involving Nmap and Scapy. 
The objective of this exercise was to apply fundamental concepts in network reconnaissance, packet analysis, and virtual network configuration using a structured, hands-on approach.
All tasks were conducted within a Kali Linux virtual environment connected to an internally configured VirtualBox network, allowing for controlled experimentation and accurate analysis of network behavior.

The Nmap component of the lab focused on rediscovering key network scanning techniques and understanding how different scan types reveal information about a target host.
I began by verifying active systems on the subnet through a host discovery scan using “nmap -sn 10.6.6.0/24.” 
After identifying the target, I executed a SYN stealth scan (“sudo nmap -sS 10.6.6.23”) to enumerate open ports in a minimally intrusive manner.
I then performed service and version detection using “sudo nmap -sV 10.6.6.23,” which provided detailed insight into the applications running on detected ports. 
To deepen the analysis, I used “sudo nmap -O 10.6.6.23” for OS fingerprinting, enabling Nmap to infer the target operating system based on TCP/IP characteristics.
Finally, I ran a basic vulnerability assessment using the Nmap Scripting Engine through “sudo nmap --script=vuln 10.6.6.23.” 
All outputs have been captured and organized within this repository to demonstrate each phase of the reconnaissance process.

The Scapy portion of the lab introduced packet-level interaction and analysis.
Using Scapy, I crafted a custom ICMP packet with the command “send(IP(dst='10.6.6.23')/ICMP()/‘This is a test’)” and transmitted it across the internal network. 
This allowed me to manually generate traffic and observe its behavior from both sending and receiving perspectives.
I then used the sniffing functionality (“sniff(iface='enp0s8', count=10')”) to capture packets traversing the assigned network interface. 
Packet details were examined using the “packet.show()” function, which displays the internal structure of captured packets, and the “a.nsummary()” method, 
which provides a summarized and indexed view of the sniffed traffic. A complete Scapy automation script, “scapy_scripts.py,” is included in this repository for reference and reproducibility.

All relevant screenshots—including Nmap scan results, Scapy captures, packet summaries, and network interface configurations—have been compiled and stored systematically in the screenshots directory.
This ensures that every step of the investigation is fully supported by visual evidence and clear documentation.

This practical assignment significantly enhanced my understanding of network scanning methodologies, packet construction, and traffic analysis. 
It also reinforced my ability to troubleshoot virtual network interfaces, interpret scan outputs, and translate technical findings into well-structured documentation. 
The combination of the theory knowledge and hands-on practice provided meaningful insight into how these tools support real-world cybersecurity operations, 
particularly in penetration testing, vulnerability assessment, and network diagnostics. Links to my GitHub repository and reflection post will be added here upon submission.
