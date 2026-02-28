---
icon: globe
---

# lilica\_04\_domain

### Challenge overview

Lilica ran a personal website linked from her social media account @twilight\_lilica. Your task is to determine when the domain name of her personal website was registered in YYYY/MM/DD format.

Flag format:

```
SWIMMER{YYYY/MM/DD}
```

***

### Initial assumptions

From lilica’s social media activity, she linked to a domain that appears to be a personal portfolio or profile site: twilight-lilica.com.

To determine the registration date, a domain WHOIS lookup (not IP WHOIS) needed to be performed. Domain WHOIS information typically includes creation/registration dates, which satisfy the challenge requirement.

***

### Investigation process

1. I located lilica’s personal website link from her social media account:

```
https://twilight-lilica.com/
```

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 2.05.39 am.png" alt=""><figcaption></figcaption></figure>

2.  I visited the site and confirmed it appeared to be associated with lilica (portfolio/profile).

    ![](<../.gitbook/assets/Screenshot 2026-01-18 at 2.07.06 am.png>)
3. I performed a domain WHOIS lookup for twilight-lilica.com. Reliable domain WHOIS sources display the creation (registration) date of the domain.
4. The WHOIS results showed the following key information:

* Domain: twilight-lilica.com
* Registered On: 2025-10-05
* Updated On: 2025-10-05
* Expires On: 2026-10-05
* Registrar: GMO Internet Group, Inc. d/b/a Onamae.com
*   Name servers: ns1.value-domain.com, ns2.value-domain.com



    <figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 2.06.34 am.png" alt=""><figcaption></figcaption></figure>

This confirmed that the domain was originally registered on 2025/10/05.

***

### Key findings

* The domain twilight-lilica.com is directly linked from lilica’s social profile.
* A WHOIS lookup revealed that the domain was registered on 2025/10/05.
* The registration data is publicly available and lawfully retrievable via WHOIS.

***

### Final flag / answer

```
SWIMMER{2025/10/05}
```

***

### Notes & takeaways

* Domain WHOIS is the authoritative source for domain registration dates, unlike IP WHOIS which provides hosting provider details (not applicable for domain creation dates).
* It’s important to differentiate between domain creation (what the challenge asks) and hosting records (which may show server providers but not domain age).
* The WHOIS record showed privacy protection for contact details, but the registration date was still visible, which fulfills the objective.
