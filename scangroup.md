## Results of basic scans of groups 1 website ##

Group 1 provided us with their website information (https://dev8773.d2d6ymu8mykhhu.amplifyapp.com/) to do some basic scanning. Since we are residing at different locations (Germany, Netherlands and Nigeria) we decided that each member carries out their own scanning, so we can compare the effect of location and time zones.

Nils did his scanning from Düsseldorf, Germany and could reach the website in 3 hops using tracert. The biggest delay hereby was the third hop with 14ms.This latency could be caused by distance (as the website server is in the US, hosted by Amazon) or by bandwidth limitations. The ping resulted Minimum = 87ms, Maximum = 94ms, Middle= 90ms. There was no detectable MX record. A whois search (https://whois.domaintools.com/) showed that most information was redacted for privacy.


Haroun carried out his scanning from Lagos, Nigeria and was successful in reaching the website in 30 hops using traceroute. The most significant delay in this exercise was the 30th hop at 133.44ms. There was no MX record identified.

Adrian did a scan from the Netherlands and in this particular example had 17 hops till the destination. That is due to the fact  the website is hosted in AWS and using cloud front to deliver the website to different regions efficiently. CloudFront is a CDN (Content Delivery Network) service that speeds up distribution of your website using own amazon datacenter infrastructure from edge locations. (What is Amazon CloudFront? - Amazon CloudFront, 2021). Due to this fact the results are different depending where the scanning is done. Destination IP address is also different depending on the location the scanning is being done due to the same reason as mentioned above. CloudFront has multiple endpoints at edge location in amazon infrastructure thus having different destination IPs for this particular FQDN (fully qualified domain name). We have also noticed multiple A records entries for the website and this is also due to CloudFront where multiple entries are used for redundancy purposes. Due to privacy regulations we can see that the contact registered for this domain is general as well as no MX entries present due to the fact that the domain does not serve mail purposes. 


References: 

Docs.aws.amazon.com. 2021. /What is Amazon CloudFront? - Amazon CloudFront/. [online] Available at: https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html [Accessed 5 September 2021].
