# Nmap and Scapy Practical Lab Documentation

This repository provides a comprehensive and professionally structured documentation of my practical laboratory work with Nmap and Scapy, carried out within a Kali Linux virtual environment connected to an isolated VirtualBox internal network. 
The objective of this lab was to apply key concepts in network reconnaissance, packet analysis, and virtual network configuration through hands-on implementation. 
Using Nmap, I rediscovered essential scanning techniques, beginning with host discovery using “nmap -sn 10.6.6.0/24” to identify active systems on the subnet, followed by a SYN stealth scan (“sudo nmap -sS 10.6.6.23”) to enumerate open ports in a low-fingerprint manner.
I further performed service and version detection with “sudo nmap -sV 10.6.6.23,” utilized OS fingerprinting through “sudo nmap -O 10.6.6.23,” and concluded with a basic vulnerability scan using the Nmap Scripting Engine (“sudo nmap --script=vuln 10.6.6.23”).
All results have been organized in this repository to illustrate each phase of the scanning workflow. The Scapy portion of the lab involved packet crafting, transmission, and inspection at a granular level.
I generated a custom ICMP packet using “send(IP(dst='10.6.6.23')/ICMP()/‘This is a test’)” to observe network behavior from a controlled source, captured traffic using “sniff(iface='enp0s8', count=10),” and
analyzed packet structures with “packet.show()” and summarized views using “a.nsummary().”
A complete automation script (“scapy_scripts.py”) is included for reproducibility.
All screenshots covering scans, packet captures, interface configurations, and analysis outputs—are systematically stored in the screenshots directory for clarity and verification.
This practical exercise strengthened my understanding of network scanning, packet-level traffic analysis, and virtual network troubleshooting while enhancing my ability to interpret technical outputs and translate them into structured, professional documentation.
The combined approach of theory and hands-on work provided valuable insight into how tools like Nmap and Scapy support real-world cybersecurity operations, particularly in penetration testing, vulnerability assessment, and network diagnostics.
