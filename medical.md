## Medical IoT Vunerabilities

The report “Compromising a Medical Mannequin” (Glisson et al., 2015) explores the vulnerabilities of medical equipment. The researcher used a medical training mannequin as a stand in for the increasing number of IoT devices in the medical field. Then the researcher tried to breach the security of this medical device in a live environment using the most common forms of attack:

Live CD brute force attack/Virtual machine brute force attack
Denial of service attack
Brute force attack
A live CD was used to gain access to the network via a brute force attack. A change in the wireless network authentication protocol to RADIUS can prevent a breach (Castillo-Velazquez, et al., 2019). RADIUS requires credentials to authenticate the user in the network. These credentials are stored in the RADIUS and ideally only the people who need to use the mannequin should have the appropriate rights.

DoS

The last attack took the form of a denial of service to target the availability. While the previously mentioned change to RADIUS would be a valid mitigation strategy, a firewall can block excessive requests. As Nikolskaya et al. (2017) states, to filter malicious traffic, various software and hardware are used, which are based on quantitative and qualitative analysis of traffic.

Another important and more general mitigation strategy is to implement security policies throughout the organization. This ranges from password policies, regular security audits to staff training. Requiring a multi factor authentication to authorize users increases password security and makes it harder for cybercriminals to impersonate users or brute force passwords (Dasgupta et al., 2017).

To sum up, the paper showed several vulnerabilities with the wireless network of the medical device. However, there are several mitigation strategies to prevent breaching the security.

 

Castillo-Velazquez, J.-I., Garcia, M. A. and Serrano Martinez, D. J. (2019) ‘Hardening as a best practice for WLAN Security Meanwhile WPA3 is released’, in 2019 IEEE 39th Central America and Panama Convention (CONCAPAN XXXIX). 2019 IEEE 39th Central America and Panama Convention (CONCAPAN XXXIX), pp. 1–5. doi: 10.1109/CONCAPANXXXIX47272.2019.8977073.

Nikolskaya, K. Yu. et al. (2017) ‘Review of modern DDoS-attacks, methods and means of counteraction’, in 2017 International Conference ‘Quality Management,Transport and Information Security, Information Technologies’ (IT QM IS). 2017 International Conference ‘Quality Management,Transport and Information Security, Information Technologies’ (IT QM IS), pp. 87–89. doi: 10.1109/ITMQIS.2017.8085769.

Dasgupta, D., Roy, A. and Nag, A. (2017) ‘Multi-Factor Authentication’, in Dasgupta, D., Roy, A., and Nag, A. (eds) Advances in User Authentication. Cham: Springer International Publishing (Infosys Science Foundation Series), pp. 185–233. doi: 10.1007/978-3-319-58808-7_5.

Glisson, W., Andel, T., McDonald, T., Jacobs, M., Campbell, M. & Mayr, J. (2015) Compromising a Medical Mannequin. Healthcare Information Systems and Technology (Sighealth).

