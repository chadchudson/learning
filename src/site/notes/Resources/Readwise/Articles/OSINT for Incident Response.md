---
{"dg-publish":true,"permalink":"/resources/readwise/articles/osint-for-incident-response/","tags":["articles","til","dfir","incidentResponse","InfoSec","Useful","Tools"]}
---

![rw-book-cover](https://www.blackhillsinfosec.com/wp-content/uploads/powerpress/BHIS_logo_podcast.png)
URL: https://www.blackhillsinfosec.com/osint-for-incident-response-part-1/
> [!abstract] Document Notes
> OSINT for IR

> my email enumeration secret weapon: “Name Server Lookup” (ba-dum-bum-ching!). Yep, good ‘ol “nslookup.” I just want to enumerate their mail server. Super quick and easy, from Linux or Windows, specify “MX” (Mail Exchanger) record type and a reliable public DNS source (Google DNS in the example below), and mash “Enter!” (about 15 seconds start to finish): ([View Highlight](https://read.readwise.io/read/01hh57q9xzyprqgyhgbg4n7hn0))

> I like *DNS Dumpster* for this next step because it’s quick, easy to use, and easy to interpret. I’m most interested in “ISP-allocated” IP blocks, e.g. “COMCAST-1234” or “LOCALISP-AS-01,” as opposed to CLOUDFLARENET, MICROSOFT-CORP, etc. Not that I’ll ignore the latter, but self-hosted/on-prem infrastructure seems to be the likelier devil’s playground. And, of course, I’ll take copious notes, screenshots, etc., of everything I learn for future reference (spoiler alert… this is important to this case!): [https://dnsdumpster.com](https://dnsdumpster.com) ([View Highlight](https://read.readwise.io/read/01hh587hzgr6ymjf6ejt2hg49h))

> If you don’t have a *Shodan.io* account, then you can’t use search filters, which presents a bit of a challenge. But you can still search for an IP or TLD. Worst-case scenario, you can filter via an alternative, then re-visit *Shodan.io* with an IP of interest (see options below): [https://shodan.io](https://shodan.io)
> ![](https://www.blackhillsinfosec.com/wp-content/uploads/2023/12/Picture3.png)
> Sample Shodan.io IP Range Search
> I used a range, as above, or you can use a “net:10.1.0.128/25” filter. From there, I reviewed ‘TOP PORTS’ for standouts. Common ports like 80 and 443 aren’t very exciting and just go in my notes. I’m more interested in unusual ports or remote-access ports, like 445, 3389, or 22. In this case, I saw two that were noteworthy: 3389 (Remote Desktop Protocol) and what looked like a non-standard web-services port. Next, I clicked on port “3389” to see associated IP addresses, then clicked on an IP for details. It’s important that you check and document the “last seen” dates. Copious notes and screenshots are your friend! ([View Highlight](https://read.readwise.io/read/01hh58aw3d45dmj5e2dfh33r4j))

> *Censys* and *LeakIX* are a couple options, both providing search capabilities without registering and a bit more functionality upon free registration:
> *Censys.io* example: [https://search.censys.io](https://search.censys.io) – ‘ip: [10.1.0.129 to 10.1.0.140]’ or ‘ip: 10.1.0.128/25’
> ![](https://www.blackhillsinfosec.com/wp-content/uploads/2023/12/Picture5.png)
> Example IP Range Search on Censys
> *LeakIX.net* example: [https://leakix.net](https://leakix.net) “Service” – ip:”10.1.0.128/25”
> ![](https://www.blackhillsinfosec.com/wp-content/uploads/2023/12/Picture6.png) ([View Highlight](https://read.readwise.io/read/01hh58bt8mxe1js3v4ggzpn77e))

