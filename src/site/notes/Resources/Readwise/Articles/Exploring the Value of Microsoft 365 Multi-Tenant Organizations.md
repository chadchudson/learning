---
{"dg-publish":true,"permalink":"/resources/readwise/articles/exploring-the-value-of-microsoft-365-multi-tenant-organizations/","created":"","updated":""}
---

![rw-book-cover](https://s36505.pcdn.co/wp-content/themes/practical365v2/images/favicon.ico)
URL: https://practical365.com/multi-tenant-organizations-value/

> five tenants ([View Highlight](https://read.readwise.io/read/01ha5davbbf7311kx18yv48d4x))

> However, the account’s calendar is inaccessible because Exchange Online tries to connect to the calendar in the mailbox of the home tenant. ([View Highlight](https://read.readwise.io/read/01ha5dekxhyympfyh94wzgswh5))

##### Note:: This seems like it defies the purpose?

> The point is that apart from the trust placed in a guest account by the person who created it, an average user cannot take the presence of a guest account in their tenant as any indication of its trustworthiness. ([View Highlight](https://read.readwise.io/read/01ha5dhrer3efmnqe5ewdwtc61))

##### Note:: CTS currently has guest access disabled anyway, reducing functionality.

> External federated chat is even less trustworthy. The fact that an external person can use Teams doesn’t tell you anything about who they are or what harm they could do. Some security researchers have illustrated how it’s [possible to send malware via federated chat](https://practical365.com/practical-protection-two-routes-to-avoiding-malware-in-teams/), which is why I recommend that organizations consider [restricting external access to known domains](https://practical365.com/teams-external-access-powershell/). The process of managing the set of permitted domains can be painful, even using PowerShell scripts, but it’s better than leaving a potential route into Teams for attackers to explore. ([View Highlight](https://read.readwise.io/read/01ha5djq3f7h9ezfedn22mvnxa))

##### Note:: This is what I was really worried about and almost made a note earlier, but was hoping they addressed it. This is a significant risk, especially, looking back at our last simulated phishing exercises.

> The Question of Tenant-to-Tenant Migrations
> Some have asked if multi-tenant organizations remove the need for [tenant-to-tenant (T2T) migrations](http://www.quest.com/products/on-demand-migration/). I don’t think so. By their very nature, T2T projects:
> • Span much more than user accounts in directory synchronization – Microsoft 365 groups, security groups, distribution lists, contacts (and maybe public folders), and so on are included in the information exchanged between tenants.
> • Can involve more than five tenants.
> • Move user accounts and other objects from one tenant to another, including personal data like mailboxes, Teams chats, and OneDrive for Business accounts.
> • Move data in shared repositories like SharePoint Online sites and Teams from one tenant to another.
> • Remove protection (sensitivity labels) from transferred data.
> • Can transfer other intellectual property like scripts, programs, and automation runbooks. ([View Highlight](https://read.readwise.io/read/01ha5dnntv2q7816p14429y00v))

##### Note:: Migration still recommended.

