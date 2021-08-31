### Medical IoT Vunerabilities

My initial post was about firewalls and demilitarized zones (DMZ) as tools to increase network security. I have described how firewalls can limit outbound and inbound data to keep unwanted data such as malware outside the network (Stewart, 2014). A DMZ is a subnet deployed between the internal network and an outside network (Anderson 2008).
Steven Johnson provided insightful information about potential mitigation about the inherent weakness of a DMZ that is the passthrough of data. His solutions include "data diodes" which is a hardware-based technology only letting data passthrough in one direction (Scott, 2015). Another technology he mentioned was the idea of placing a honeypot in the DMZ to purposefully attract attackers to detect their presence in the network (ISC, 2015).
One downside of firewalls is, that they can lead to reduced network speed (Saidin & Zolkipli, 2017).
Shota Kameyama addressed this in his reply and suggests that building a high-performance firewall can decrease latency. For example, a next generation firewall (NGF) can track end user’s identity, provide real-time data protection and identify applications with a better network performance as compared to traditional firewalls (Talim 2019).
Haroun Fujah suggested to further increase network security with a dual firewall approach. Using two distinct different firewall setups between the DMZ prevents the cyber-criminal to use the same approach on the outer and inner firewall (Noonan and Dubrawsky, 2006). 
Megan McClintock’s contribution had a different approach which included adding a intrusion detection systems to a firewall systems. This system is a more active approach to network security, since it purpose is to discover how the network was breached (Grace 2000). 
In conclusion, I can state that a combination of all technologies as described by my and my fellow students would provide a solid network security. Such a network would contain a DMZ with a honeypot, a double firewall and an IDS. However, this means increased configuration and operation. Further if such a layered approach impairs network performance would be subject to further research.

References:

Stewart, M. J. (2014) Network Security, Firewalls and VPNs. Available from: https://books.google.com/books/about/Network_Security_Firewalls_and_VPNs.html?id=qZgtAAAAQBAJ [Accessed: 10 June 2021].
Anderson, Ross (2008) Security Engineering : A Guide to Building Dependable Distributed Systems. Indianapolis, IN: Wiley. Available from: http://search.ebscohost.com/login.aspx?direct=true&db=nlebk&AN=343359&site=ehost-live.
Scott, A, SANS Reading Room (2015) Tactical Data Diodes in Industrial Automation and Control Systems. Available from:  https://www.sans.org/reading-room/whitepapers/firewalls/tactical-data-diodes-industrial-automation-control-systems-36057 [Accessed June 24th, 2021]
(ISC)2 (2015) Official (ISC)2 Training Guide CISSIP CBK (ISC)2 Press
Talim, K. (2019) Enhanced Network Security Using Next Generation Firewalls (NGFW). Available from: http://dspace.daffodilvarsity.edu.bd:8080/bitstream/handle/123456789/4908/P15188%20%2826_%29_.pdf?sequence=1&isAllowed=y [Accessed: June 24th, 2021].

Noonan, W. J., Noonan, W., & Dubrawsky, (2006). Firewall Fundamentals. Cisco. 
Grace, C., 2000. Understanding Intrusion Detection Systems. [online] Techsupportalert.com.
Available from: [Accessed24th June 2021].

