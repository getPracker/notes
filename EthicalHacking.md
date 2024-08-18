Penetration testing (pentesting for short) 
is when an organization hires one or more ethical hackers to try to break into their network and provide feedback on improving security. This is a simulated cyber attack conducted to identify security weaknesses. Pentesting uses the same skills and knowledge malicious hackers use when conducting real cyberattacks.

When a new piece of malware comes out, it needs to be studied and analyzed so that we can defend against it. Malware analysts are hackers who, as we might infer, analyze malware. Of course, the hackers who write the malware don’t want their malware to be analyzed and take steps to hamper the efforts of analysts. As such, malware analysts need to be familiar with the techniques used to create and obfuscate malware to do their job.

Security analysts are defensive hackers, working to harden systems and protect them from attack. If an attack does occur, they are usually the first to respond. Because they often work directly against other hackers, it is not unheard of (though it is rare) for Hollywood-esque “hacker duels” to take place, with two hackers attempting to lock each other out of a network or computer.

### Intro To Bug Hunting
**The Hacking Process
2 min**  
Before we go hunting, let’s learn about the hacking process. The hacking process is a combination of ethical hacking tactics for organizational defense. Having a list of tactics to ensure organizational defenses is a helpful resource for ethical hackers and bug hunters. Ethical hackers can use these tactics to ensure the security of a system and identify potential areas of vulnerabilities and software bugs.

The hacking process consists of the following:   
1. Footprinting, also known as the “Reconnaissance” phase, is passive information gathering of targets before active attack activities.
2. Scanning is an initial active/passive inspecting technique to gather technical information on target systems.
3. Enumeration is the consolidation and gathering of more detailed information on target systems and networks.
4. System Hacking is the planning and execution of attacks conducted based on the information gathered in Footprinting, Scanning, and Enumeration.
5. Escalation of Privilege is when an attacker is successful and can gain access to the systems/networks of the organization.
6. Planting Backdoors is leaving an entry point to a compromised system for easy access to further attack activities.
7. Covering Tracks is the act of removing or destroying signs of intrusion and activities performed on a system.

**A SQL injection** is a common vulnerability affecting applications that use SQL as their database language. A hacker can use their knowledge of the SQL language to cleverly construct text inputs that modify the backend SQL query to their liking. They can force the application to output private data or respond in ways that provide intel. To specify, we will be doing a boolean-based injection that involves SQL statements that can confirm TRUE/FALSE questions about the database.

To perform a SQL injection, we will insert the following statement in the password input field:

'1' OR '1' = '1'

To resolve this vulnerability, there are two main things we can do; sanitization and parameterized queries.

Sanitization removes dangerous characters from user input, and parameterized queries are queries with placeholders used as parameters during the code execution.

### Ports and You
**2 min**
An important concept to understand for network enumeration (and networking in general) is the concept of ports. Ports are to IP addresses, what apartment numbers are to street addresses. Ports don’t specify which computer the data gets sent to, but the computer uses the port number to figure out which program to give the data to once the data arrives. Knowing what ports a computer has active can give us an idea of what services the computer is running and what the computer’s purpose is.

Here’s a summary of the most important things to know about ports:

+ There are 65536 different ports, numbered 0-65535.
+ Ports 0-1023 are reserved for the most important or well-known protocols.
+ Ports 1024-49151 are associated with less common protocols and services.
+ Ports 49152 and up are dynamic and can be used as needed.
+ Ports can be open or closed. Ports are closed by default but are opened when a computer runs a service that uses that port.
+ Services can run on ports other than the port they are associated with by default. Likewise, services can run on ports associated with different services if configured. This can be used defensively to make network enumeration more difficult or offensively to obfuscate malicious connections.

+ The situation is as follows: One of the computers in a network has been infected with malware.

Our task is to use network enumeration to determine which computer is likely to be infected so the computer can be wiped. We know the malware opens a port while it runs, but we don’t know which port. 

In this exercise, we’ll use Nmap, a popular network scanning/enumeration tool, to identify which computer needs to be wiped. We’ll be using IP addresses in 10.1.1.x range for demonstration purposes.

Before we begin our discovery, here are a few things to note:

Nmap, Network Mapper, is a port scanner/network mapping tool. It is the most used scanning tool by ethical and unethical hackers. The tool scans systems/networks for IP addresses, ports, OS details, and applications/services installed.
Nmap is an open-source command-line tool designed to run on the Linux operating system (OS).
Nmap is an open-source tool that is open to the public to use and improve on.
Note: Some of these services are not running on this box, so we have faked some terminal interactions in this specific exercise. This is so you can experience how these commands work in the real world. 

### Vulnerability Analysis & Exploitation Demo
#### Introduction
**1 min**
As an ethical hacker, we are defining, classifying, identifying, and mitigating vulnerabilities within a system or organization. These responsibilities are often identified as performing vulnerability analysis and exploitation.

Vulnerability analysis defines and classifies security threats.

Vulnerability exploitation identifies weaknesses and mitigates them within a system or organization.

If done manually, vulnerability analysis and exploitation are long and tedious. Thankfully, due to the advancement of technology, ethical hackers are given tools to perform these tasks efficiently and quickly.

Some of the tools to list are:

1. Armitage: A graphical user interface (GUI) tool for the Metasploit project that illustrates targets and offers exploits suggestions.
2. Nmap: An open-source tool for network discovery and security auditing.
3. Nikto2: An open-source command-line vulnerability scanner for web servers.
4. W3AF: An open-source web application scanner.

### Packet Sniffing Demo
Introduction
1 min
Packet sniffing is the act of logging and analyzing packets of data that are sent over a network. There are lots of different reasons you might want to do this. Attackers can use packet sniffing to reverse engineer Application Programming Interfaces (APIs) and find vulnerabilities. Defenders can use packet sniffing to look for suspicious activity on the network. Packet sniffing can also be used for troubleshooting network issues. Looking at individual sent packets can let us better understand what’s going on “under the hood”, and that knowledge can be used to fix or break things.

Additionally, it is important to note that we don’t capture and analyze simultaneously. Some defensive security systems do analyze captured traffic in real-time, but it’s not practical for us humans. When we do a packet capture, we capture traffic first and save it in the packet capture (.cap or .pcap) file and finally analyze the file.
