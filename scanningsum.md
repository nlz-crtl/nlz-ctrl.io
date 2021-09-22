## Summary of Discussion 2

Group 2, Security Squad, laid out their scanning results in the initial post. Their scanning strategy consists of doing a basic scan from different locations, to highlight potential effects of physical location. Utilizing, ping, tracert and whosis tools Group 2 shared their findings.

A particular interesting find was the difference of hops for each group member. A possible reason for that could be the use of CDN (Content Delivery Network) by Amazon Web 
Services. CDN uses different datacentre regions depending on the location of the request to speed up services.
Shota Kameyama investigated further and concluded that the differences in the number of hops happened because of contacting the origin server from each country through different routes over different border gateway protocols (BGP). Another theory he proposed was that the the CDN impacts the traceroute results.
