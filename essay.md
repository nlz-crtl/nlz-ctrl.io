
 

## ASMIS SECURITY REPORT
### Individual Essay


 
# 1.	Introduction

The queens medical centre is planning to introduce a web-based appointment and scheduling management information system (ASMIS) to improve patient care and efficiency.
Aim of this report to give an overview of potential security threats to ASMIS as well as providing a starting point for mitigation strategies.
Out of scope of this report are a fully detailed and complete analysis, physical security, extensive staff knowledge check and training.
 
2.	Benefits and potential problems regarding of the Queens medical centre’s ASMIS

To correctly assess the benefits and potential drawbacks of the Queens medical centre’s ASMIS, a superficial SWOT analyses will prove an overview. The SWOT analysis is a strategic tool and consists of internal factors (strengths and weaknesses) as well as external factors (opportunities and threats). Once these factors are outlined, the correct mitigation efforts can be planned. 
Starting with a broad overview in figure 1 and then detailing each component, the focus will shift on the relevant risks and weaknesses for this case.
 
Figure 1: SWOT analysis of ASMIS

Strengths:
•	Efficiency: The patients get directly in contact with the appropriate specialists depending on the specialist’s workload.
•	Scalability: The ASMIS is not limited by the number of people who can handle phone calls.
•	Cost savings: Using the ASMIS requires fewer employees who solely manage calls from patients.
Weaknesses:
•	IT-systems: The current IT network and hardware must be able to handle the workload of the ASMIS.
•	Data security: Internal data security is a concern. Sensitive data must not be shared between departments.
•	Additional training: Additional training is necessary for the staff which uses and administrates the ASMIS.
Opportunities
•	Data collection: The ASMIS could be use for anonymously data collection to improve patient care in peak times and for forecasting events like flu season.
•	Nationwide rollout: The ASMIS at the Queens medical centre could be use a blueprint to eventually rollout ASMIS nationwide.
Threats
•	Acceptance: There is a chance that the population will not accept the ASMIS and prefers the old system.
•	Cyberattacks: Since the process is digitalized and contains very sensitive data, ASMIS is vulnerable to cyberattacks. These attacks can come in myriad of ways and hence will be examined in detail a later chapter using threat modelling.

Regarding the threats as outlined in the SWOT analysis, the danger coming from cyberattacks is very high and likely. To illustrate this, since the COVID-19 pandemic many healthcare providers across the world have been the target of complex and coordinatized cyber-attacks (Muthuppalaniappan & Stevenson, 2021). There have also been past cyberattacks that specifically targeted the British healthcare (NHS), that generated criticism of the failing to invest in cyber security (Dwyer, 2018).
To avoid this, a detailed look at the different types of attacks that could target ASMIS is necessary.

 
# 2.	Sequence diagram of ASMIS

It was established in the SWOT analysis, that the ASMIS might be vulnerable to cyberattacks. To better understand its weaknesses against those attacks, it is necessary to capture how the data flows and how the system works. A sequence diagram shows an interaction between objects in a time sequence (Rayner et al., 2005). The diagram displays a use case within a scenario at a chosen level of abstraction (Appukkutty et al, 2005). This can provide a high-level overview of the functions and dataflow of ASMIS which then can be further deconstructed to determine potential security threats. 
 
Figure 2: Sequence diagram of ASMIS

Figure 2 shows a sequence (steps 1-12) of a use case of ASMIS in which a patient books an appointment at the Queens medical centre with an specialist doctor. It goes through all necessary steps of the process from the patients (primary actor), ASMIS (UI) and databank (backend) perspective. It lacks the underlying network of servers, interfaces and databases involved but offers an easy-to-read starting point. Furthermore, it can also serve as a first step to decompose an application in single steps which then can be used in a STRIDE analysis as well as in threat modelling (Howard, et al., 2014).
With the knowledge how a normal sequence is processed, a STRIDE analysis can be modelled to identify potential cyber security threats.
 
# 3.	STRIDE analysis of ASMIS

The identified processes and dataflows in the sequence diagram (figure 2) can now be used as targets in a STRIDE analysis. STRIDE is an acronym derived from the following threat categories (Microsoft, 2009):
•	Spoofing Identity
•	Tampering with Data
•	Repudiation
•	Information disclosure
•	Denial of service 
•	Elevation of privileges
The STRIDE analysis is especially useful for inspecting each system component for vulnerabilities which could comprise the whole system (Khan et al., 2017). For this case study, the focus is on the in figure 2 outlined processes.
 
Figure 3 STRIDE analysis
Figure 3 shows a selection of potential attacks on the ASMIS system according to the STRIDE analysis. To further understand threats to the system and determine who can carry out such attacks an abuse needs to be created. 
4.	Abuse case diagram of ASMIS

McDermott & Fox (1999) defines an abuse case as a specification of a type of complete interaction between a system and one or more actors, where the results of the interaction are harmful to the system, one of the actors, or one of the stakeholders in the system. An abuse typically includes a malicious actor (as opposed to the normal use case actor), a description of the of security privileges that may be abused and a description of the harm. The abuse case diagram can be used to explore weaknesses which then can be mitigated by using suitable countermeasures (Tøndel et al., 2010). 
However, one downside which is important to note, is that abuse case diagrams tend to produce fewer overall identified threats. On the other hand, abuse cases are more inclined to identify problem-specific threats and included user-oriented and organisational threats (Sindre et al., 2003).
This is an advantage the case of Queens medical centre’s ASMIS, since it is very user oriented and integral to the organisation.
 
Figure 4 Abuse case diagram


# 4.1 Actor description

Malicious staff: A malicious user from inside the organization with the possibility of having already authorized access to the ASMIS system.
Cybercriminal: An attacker from outside the organization without authorized access to the ASMIS system and the intention to do harm.


Malicious staff abuse cases
Case:	Harm:
Delete important data	Disrupt workflow, 
Expose sensitive data	Breach of data confidentiality, damage reputation
Table 1 malicious staff abuse cases

Cyber Criminal abuse cases
Case:	Harm:
DDoS attack	Disrupt workflow, service not available
Brute force password	Unauthorized access to the system
Intrude system	Deploy malware:
•	Slow network, send spam, spread through network.
Deploy ransomware:
•	Encrypt sensitive data, extortion 
Impersonate Users	Steal data, damage reputation
Table 2 cybercriminal abuse cases
 
# 5.	Threat Tree

The abuse case diagram (figure 4) showed potential malicious actors and their intentions to cause harm to the ASMIS system. A threat tree can help understanding the decision making an attacker goes through to archive their target. Once a threat is completely understood, mitigating technologies can be deployed (Howard et al. ,2014).
Threat trees are a very common tool to understand and eventually mitigate cyber-attacks. Despite its widespread use there is no standardized visual configuration (Lallie et al., 2020). One benefit of threat trees is its easy-to-read interpretation and identification of security vulnerabilities. A downside to this approach is he difficulty to display all possible actions of an attacker (Nagaraju et al., 2017).
The threat tree shows the target on top and the steps to achieve this target in its branching limbs. At the bottom of the tree there are the security weaknesses which are the ways how a malicious actor can attack.
Figure 5 displays a threat tree which has data as its target. Whether the attacker aims to tamper with data, expose sensitive information or wants to encrypt data for extortion this tree shows the possible ways to achieve its target. 
 
Figure 5 Threat tree data

Threat tree data
Threat target	Sensitive Data, information about patients and specialists.
Threat category	Tampering, information disclosure, spoofing elevation of privilege.
Risk
	Very high, very likely.
Mitigation techniques	Password policy, staff training, firewalls and IDS, encryption and data masking.
Comment	Sensitive patient information is a high value target and has been targeted by cyber criminals in the past.
Table 3 Threat tree data details

Figure 6 displays a threat tree which has ASIMIS’s availability as its target. Here the attacker aims to interrupt or deny the availability of the system to its users.
 
Figure 6 Threat tree availability

Threat tree availability
Threat target	Availability of ASMIS services.
Threat category	Denial of services
Risk
	High, very likely.
Mitigation	Firewalls and IDS, business continuity policies, load balancers.
Comment	Continuous service is vital to the Queen’s Medical Centre since it is critical infrastructure.
Table 4 Threat tree availability details

The threat trees expose the decision-making process and security vulnerabilities that cyber criminals use. With that knowledge, appropriate mitigation techniques can be deployed, which will be discussed in the next chapter.
 

# 6.	Mitigation strategies

Based on the security weaknesses exposed in figure 5 and 6 the following security features should be deployed to protect ASMIS from cybercriminals:
•	Firewalls
•	IDS
•	Encryption
•	DDoS protection
•	Security policies
Firewalls
Firewalls can limit outbound and inbound dataflow to the network, thus protecting it from intrusion and unwanted data such as malware or ransom software. It needs to be configured to determine which packets can pass the firewall (Stewart, 2014). In this case, several firewalls in conjunction with an DMZ to provide protection and segmentation should be deployed. On potential downside of firewalls is that they reduce overall network performance.

IDS
Intrusion detection systems take a more active role in protecting ASMIS from cybercriminals. It can discover how the attacker penetrated the network and limit harm (Grace, 2000). IDS needs to be configured and tailored to ASMIS, so that only the use case shown in figure 2 shall pass. It should also be considered that a IDS can lead to a flood of false positive alarms which have to be examined in detail

Encryption
All sensitive data, weather in transport or at rest, should be encrypted to prevent authorized access. Especially the data in transport between the patients and the specialists which moves through the internet should have an end-to-end encryption to prevent unwanted disclosure of this data (Troncoso, 2019).

DDoS protection
DDoS protection can take several forms. A firewall for example, can block excessive requests. As Nikolskaya et al. (2017) states, to filter malicious traffic, various software and hardware are used, which are based on quantitative and qualitative analysis of traffic. Filtering can slow down the flow of data in the network, that is why it is suggested that resource intensive tasks are moved on dedicated servers, to avoid bottlenecks.

Security policies
Another important aspect is to implement security policies throughout the organization. This ranges from password policies, regular security audits to staff training. Requiring a multi factor authentication to authorize users increases password security and makes it harder for cybercriminals to impersonate users or brute force passwords (Dasgupta et al., 2017). To ensure business continuity, hardware redundancies and protection against outage should be implemented.

Further considerations
As a further consideration utilizing cloud technology should be considered. Moving to the cloud has several benefits such as scalability, increased redundancy, and physical security as well as advanced security options such security-as-a-service.

 
# 7. Conclusion

ASMIS offers a lot of advantages and could be a great benefit to Queens Medical centre. However, the underlining IT-system needs to be hardened against attacks from cybercriminals. The sensitive data ASMIS utilizes is an attractive target for malicious actors. Several ways how cybercriminals could achieve their goals are explored in the threat trees.
It is vital that Queens medical Centre deploys security technologies and strategies to mitigate these potential threats. This report gave a selection of mitigation approaches which should be further examined, since the field of cybersecurity is everchanging. 
 
# 8. References

Appukkutty, K., Ammar, H. H. and Popstajanova, K. G. (2005) ‘Software requirement risk assessment using UML’, in The 3rd ACS/IEEE International Conference onComputer Systems and Applications, 2005. The 3rd ACS/IEEE International Conference onComputer Systems and Applications, 2005:112-. doi: 10.1109/AICCSA.2005.1387101.
Dwyer, A. C. (2018) ‘The NHS cyber-attack: A look at the complex environmental conditions of WannaCry’, RAD Magazine, 44. Available at: https://ora.ox.ac.uk/objects/uuid:865b4aae-dc23-4335-82c5-6b5b269f3301 [Accessed: 27 June 2021].
Howard, M., LeBlanc, D. and LeBlanc, D. (2014) Writing Secure Code : Practical Strategies and Proven Techniques for Building Secure Applications in a Networked World. Redmond, UNITED STATES: Microsoft Press. Available at: http://ebookcentral.proquest.com/lib/universityofessex-ebooks/detail.action?docID=540974.
Khan, R. et al. (2017) ‘STRIDE-based threat modeling for cyber-physical systems’, in 2017 IEEE PES Innovative Smart Grid Technologies Conference Europe (ISGT-Europe). 2017 IEEE PES Innovative Smart Grid Technologies Conference Europe (ISGT-Europe): 1–6. doi: 10.1109/ISGTEurope.2017.8260283.
Lallie, H. S., Debattista, K. and Bal, J. (2020) ‘A review of attack graph and attack tree visual syntax in cyber security’, Computer Science Review, 35, p. 100219. doi: 10.1016/j.cosrev.2019.100219.
Microsoft (2009) The STRIDE Threat Model. Available at: https://docs.microsoft.com/en-us/previous-versions/commerce-server/ee823878(v=cs.20) [Accessed: 29 June 2021].
Muthuppalaniappan, M., LLB and Stevenson, K. (2021) ‘Healthcare cyber-attacks and the COVID-19 pandemic: an urgent threat to global health’, International Journal for Quality in Health Care, 33(1). doi: 10.1093/intqhc/mzaa117.
Nagaraju, V., Fiondella, L. and Wandji, T. (2017) ‘A survey of fault and attack tree modeling and analysis for cyber risk management’, in 2017 IEEE International Symposium on Technologies for Homeland Security (HST). 2017 IEEE International Symposium on Technologies for Homeland Security (HST): 1–6. doi: 10.1109/THS.2017.7943455.
Rayner, M. et al. (2005) ‘OMG Unified Modeling Language Specification’, in Version 1.3, © 1999 Object Management Group, Inc.
Sindre, G., Firesmith, D. G. and Opdahl, A. L. (2003) ‘A reuse-based approach to determining security requirements’, in REFSQ. Citeseer: 127–136.
Tøndel, I. A., Jensen, J. and Røstad, L. (2010) ‘Combining Misuse Cases with Attack Trees and Security Activity Models’, in 2010 International Conference on Availability, Reliability and Security. 2010 International Conference on Availability, Reliability and Security: 438–445. doi: 10.1109/ARES.2010.101.
Stewart, M. J. (2014) Network Security, Firewalls and VPNs. Available at: https://books.google.com/books/about/Network_Security_Firewalls_and_VPNs.html?id=qZgtAAAAQBAJ [Accessed: 10 June 2021].
Grace, C. (2000) ‘122 - Understanding intrusion detection systems’, (122), p. 5.

Troncoso, C. (2019) ‘Privacy & Online Rights Knowledge Area Issue 1. The Cyber Security Body of Knowledge.’ Available at: https://www.cybok.org/media/downloads/Privacy__Online_Rights_issue_1.0_FNULPeI.pdf.
Nikolskaya, K. Yu. et al. (2017) ‘Review of modern DDoS-attacks, methods and means of counteraction’, in 2017 International Conference ‘Quality Management,Transport and Information Security, Information Technologies’ (IT QM IS). 2017 International Conference ‘Quality Management,Transport and Information Security, Information Technologies’ (IT QM IS): 87–89. doi: 10.1109/ITMQIS.2017.8085769.
Dasgupta, D., Roy, A. and Nag, A. (2017) ‘Multi-Factor Authentication’, in Dasgupta, D., Roy, A., and Nag, A. (eds) Advances in User Authentication. Cham: Springer International Publishing (Infosys Science Foundation Series): 185–233. doi: 10.1007/978-3-319-58808-7_5.

