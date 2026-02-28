---
icon: vr-cardboard
---

# lilica\_02\_virtual\_identity

### Challenge overview

Lilica is also interested in VR, and some activity has been observed in the future. The objective of this challenge is to identify **the VRChat user ID which lilica was using as of 2026**.

VRChat user information can be viewed in a web browser.

Flag format:

```
SWIMMER{VRCHAT_USER_ID}
```

Example (not the solution):

```
SWIMMER{usr_xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}
```

***

### Initial assumptions

* Lilica may use the same or similar username across platforms.
* VRChat profiles are publicly searchable, but require login to access the full user search.
* The goal is to retrieve the **user ID**, not display name.

***

### Investigation process

1. I registered an account on **VRChat** to access the user search functionality.
2. Using lilica’s X/Twitter display name: `黄昏ブロッサムリリカ`, I searched for the user inside VRChat.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 2.14.48 am.png" alt=""><figcaption></figcaption></figure>

3. Once located, I accessed the profile URL which contained the **user ID**.

URL found:

```
https://vrchat.com/home/user/usr_b103fac6-8341-4b89-a606-920092e75e43
```

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 2.15.01 am.png" alt=""><figcaption></figcaption></figure>

***

### Key findings

* Lilica’s VRChat account as of 2026 has the user ID: `usr_b103fac6-8341-4b89-a606-920092e75e43`.
* The user ID is embedded in the profile URL and is publicly retrievable with a VRChat account.
* No direct interaction with the user was required.

***

### Final flag / answer

```
SWIMMER{usr_b103fac6-8341-4b89-a606-920092e75e43}
```

***

### Notes & takeaways

* Usernames and display names can differ from the unique system ID in VRChat; always verify the ID from the profile URL.
* Creating a free account is necessary to access VRChat’s internal search, which is a **lawful OSINT method**.
* This demonstrates how cross-platform identity correlation can be performed using only publicly accessible information.
