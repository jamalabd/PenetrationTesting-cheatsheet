# What is Penetration testing ?

## Introduction

The reference is your key to a comprehensive understanding of the Notion API.

<aside>
🤔 Penetration testing or Pen testing is a security exercise where a cyber security experts attempts to find and exploit a security vulnerabilities.

</aside>

### Day to day as a Pentester

The day to day of a Pentester consists of:
1: `Perform an assessment`, 
2: `Write a report`, 
3: `Give a debrief`  

**Perform an Assessment**

- External Network Pen Test
    - This is assessing an organizations security from the outside ( out side of that organization ) 🤔 think hacker sitting in a coffee shop attempting to break into the security system of a bank across the street.
    - The most common type of pentest and usually the one they start you with as beginner.
    - Focused heavily on [OSINT](https://www.sans.org/blog/what-is-open-source-intelligence/) ( Open Source Intelligence ) gathering techniques. This is information you can get openly. Investigating the origination and its history maybe it was involved in a past breach and why, could we get those breached accounts and try to use those passwords, or investigate its employees maybe theres an employee who speaks online about his hate for the company and would readily give you information. Can we collect data and use it against the organization.
    - Most common because most complacence organizations require that an external pentest be done annually, the other reason is these are usually cheeper then the other forms of pentesting.
    - This form of testing usually last 32 - 40 hours with 8 - 16 hours for report writing.
- Internal Network Pen Test
    - This is assessing an organizations security from the inside of the network. Meaning we some how breached to perimeter (ex: via fishing email or some other ).
    - Focuses heavily on [active directory attacks](https://book.hacktricks.xyz/windows-hardening/active-directory-methodology). Most companies use this method for internal pentests and are essential for you to know.
    - This form of testing usually last 32 - 40 hours with 8 - 16 hours for report writing.
- Web Application Pen Test
    - This is assessing an organizations web security.
    - Focuses heavily on web based attacks and [OWASP](https://github.com/OWASP/wstg) testing guidelines. It is essential that you know the OWASP [Top 10 Attacks](https://www.reflectiz.com/blog/owasp-top-ten-2023/).
    - This form of testing usually last 32 - 40 hours with 8 - 16 hours for report writing.
- Wireless Network Pen Test
    - This is assessing an organizations wireless network security.
    - [Methodology](https://imshewale.medium.com/complete-wifi-hacking-methodology-14d1f44715b7) varies depending on what type of wireless network there using. Guest
    VS WPA2-PSK vs WPA2 Enterprise.
    - This form of testing usually last 4 - 8 hours per SSID with 2 - 4 hours for report writing.
- Physical & Social Engineering Pen Test
    - This is assessing an organizations physical security.
    - Going on site and trying to break into the building. From cloning badges to picking locks. This all depends on the clients Goal
    - This form of testing usually last 16 - 40 hours with 4 - 8 hours for report writing.
- Mobile Penetration Testing
- loT Penetration Testing
- Red Team Engagements
- Purple Team Engagements
- And more

**Write a report**

- A report is typically delivered within a week after the engagement ends
- Report should highlight both non technical called executive findings & technical findings
- Recommendations should be clear to both executives and technical staff.
- have presentation skills

**Give a Debrief** 

- A debrief walks through your findings. This can be with technical or non technical staff.
- It gives an opportunity for the client to ask questions and address any concerns before a final report is released.

### Networking Refresher

- **IP Adressess**
    
    Pull up IP Address by running `ifconfig` (MAC, Linux) in the terminal. 
    
    Below we we have:  IP address (ipv4 address ) - inet & IP address (ipv6 address ) - inet6. These are layer 3 protocols which is a router.
    
    The ipv4 address is in a decimal notation and ipv6 address is in a hexadecimal notation. The ipv4 is made up of 32 bits which equals 4 bytes. Each portion of numbers after the decimal is 8 bits. 
    
    <img width="761" alt="Screenshot 2023-10-11 at 1 32 45 PM" src="https://github.com/jamalabd/PenetrationTesting-cheatsheet/assets/45414121/dbb6f975-40f2-4aae-82ba-feac0a3ec5d2">

    
    Ipv6 was created to insure there would be enough Ip addresses for everyone but still to this day we relay mainly on ipv4 instead of ipv6. One personal theoretically could use 20 ip address, that is an ip address for each device connected to the internet but due to something called NAT this is not an issue essentially you have one ip address for a building and all the devices work through that one. Network Address Translation ( NAT ) we are assigned privet IP address spaces. An IP address like the above that starts with 192.168 is privet. 
    
   <img width="625" alt="Screenshot 2023-10-11 at 2 09 15 PM" src="https://github.com/jamalabd/PenetrationTesting-cheatsheet/assets/45414121/8a237b1c-e2ab-48d7-9b43-38c62597227d">

    
    Privet IP addresses are broken up into classes, A being the largest used be giant corporations & C being the smallest used for homes and small businesses. The network numbers are what you will see for an IP address at every level like stated previously 192.168 is privet and from the number of hosts per network most likely for a home or small business. Anything out side of these are public. You can rent those from your ISP ( internet service provider )

- **MAC addresses**
    
    Layer 2
    
    - MAC ( Media Access Control ) represents a physical address. MAC addresses are how we communicate over switches.
    - MAC addresses have unique identifiers. The image bellow shows the MAC address
        

      <img width="371" alt="Screenshot 2023-10-15 at 2 56 45 PM" src="https://github.com/jamalabd/PenetrationTesting-cheatsheet/assets/45414121/fa84dc2b-2cd0-4446-8dc6-7d84f0f02315">

        
    - It has 6 pairs of 2, he first 3 pairs are the identifiers. These can be used  to look up the MAC address
- **TCP VS UDP**
    
    TCP ( Transmission Control Protocol ) 
    
    - This is  a connection oriented protocol
    - Best suited for making a connection, use if need high reliability
    - Ex: HTTP ( hypertext transfer protocol ), HTTPS ( hypertext transfer protocol secure ), SSH ( secure shell ), FTP ( file transfer protocol )
    - The most commonly used protocol
    - Works on a three way handshake, `SYN > SYN ACK > ACK` your send `SYN`, They achnology you and send `SYN ACK`back the your good to start your desired action `ACK`  this is how we connect to ports
    
    UDP ( User Datagram Protocol ) 
    
    - This is a connectionless protocol
    - EX: Streaming service, DNS ( domain name system ), Voice over IP
- **Common Ports and Protocols**
    
    TCP ( Transmission Control Protocol ) 
    
    - FTP (21)
    - SSH (22)
    - Telnet (23)
    - SMTP (25)
    - DNS (53)
    - HTTP (80) / HTTPS (443)
    - РОР3 (110)
    - SMB (139 + 445)
    - IMAP (143)
    
    UDP ( User Datagram Protocol ) 
    
    - DNS (53)
    - DHCP (67, 68)
    - TFTP (69)
    - SNMP (161)
- **OSI ( Open Systems Interconnection ) Model**
    
    Please do not throw someone's pizza away 
    
    1 P - Physical layer: data cables, cat6, something you plug in
    
    2 D - Data layer: switching, MAC addresses
    
    3 N - Network layer: IP addresses, routing
    
    4 T - Transport layer: TCP / UDP
    
    5 S - Session Layer: Session management 
    
    6 P - Presentation layer: WMV, JPEG, MOV files  
    
    7 A - Applications layer:  HTTP, SMTP applications that you utilize 
    

### **Subnetting**

LOOK INTO FURTHER

Resources

https://www.youtube.com/watch?v=ZxAwQB8TZsM
https://drive.google.com/file/d/1ETKH31-E7G-7ntEOlWGZcDZWuukmeHFe/view?pli=1 
