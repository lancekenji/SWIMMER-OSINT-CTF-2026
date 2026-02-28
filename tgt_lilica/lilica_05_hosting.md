---
icon: globe-pointer
---

# lilica\_05\_hosting

### Challenge overview

Lilica hosts a personal website using a third-party hosting service. The website itself is not violating any terms, but the objective is to identify the **abuse-reporting email address** of the hosting provider.

Flag format:

```
SWIMMER{EMAIL_ADDRESS}
```

**Warning**: Do not send emails to this address. The task is only to identify it via OSINT.

***

### Initial assumptions

* The website domain is `twilight-lilica.com`.
* The challenge focuses on the hosting service, not the domain registrar.
* Hosting service contact information can be retrieved via **IP address WHOIS lookup**.
* Only publicly available, legal sources will be used.

***

### Investigation process

1. I resolved the domain twilight-lilica.com to its IP address.
2. I performed a WHOIS lookup on the IP address using ARIN and RDAP services to retrieve hosting provider information.
3. The WHOIS output provided details of the hosting provider and included **abuse contact information**. Key details extracted:

```
Organization: Vultr Holdings, LLC
Abuse Email: abuse@vultr.com
```

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 2.09.38 am.png" alt=""><figcaption></figcaption></figure>

4. This email is the canonical point of contact for reporting abuse for the hosting service, as required by the challenge.

***

### Key findings

* The hosting provider for twilight-lilica.com is Vultr Holdings, LLC.
* The publicly listed abuse-reporting email is **abuse@vultr.com**.
* This information is retrievable via lawful IP WHOIS lookup.

***

### Final flag / answer

```
SWIMMER{abuse@vultr.com}
```

***

### Notes & takeaways

* IP WHOIS provides hosting provider contact info, which is different from domain registrar WHOIS.
* The abuse email is intended only for reporting violations or issues; it should not be used casually.
* This demonstrates the value of **passive OSINT** in verifying infrastructure-related contacts without direct interaction with the target.
