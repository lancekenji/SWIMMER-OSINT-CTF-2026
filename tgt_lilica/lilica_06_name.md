---
icon: user-magnifying-glass
---

# lilica\_06\_name

### Challenge overview

The objective of this challenge is to determine **lilica’s real name** using publicly available information. The answer should be in the **Latin alphabet (romaji)**.

Flag format:

```
SWIMMER{REAL_NAME}
```

Example (not the solution):

```
SWIMMER{Sanae Takaichi}
```

***

### Initial assumptions

* Lilica shares VR-related content and accessories on her social media account **@twilight\_lilica**.
* Metadata inside downloadable VR/3D model files can contain author information.
* Only publicly accessible files and lawful OSINT methods are used.

***

### Investigation process

1. On lilica’s X account, I found a post about a VRChat accessory with a downloadable link:

```
https://54.gigafile.nu/0324-c62de7be61d9af6377e01324cec7939b5
```

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 2.20.30 am.png" alt=""><figcaption></figcaption></figure>

2. I downloaded the file and opened it using a text editor, after confirming that FBX files store metadata in readable sections.
3. Within the FBX file metadata, I found a reference to the original file path including the user name:

```
\Users\shiharu_nanaogi\Documents\modeling\vrc_test\hair_pin\simple_hair_pin.fbx
```

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 2.21.39 am.png" alt=""><figcaption></figcaption></figure>

4. The path reveals the likely real name: **Shiharu Nanaogi**.

***

### Key findings

* The FBX metadata includes the creator’s username in the file path.
* Cross-referencing the VR accessory download with the X post confirms that this file belongs to lilica.
* This is a lawful and passive OSINT method to retrieve creator information from file metadata.

***

### Final flag / answer

```
SWIMMER{Shiharu Nanaogi}
```

***

### Notes & takeaways

* FBX files often retain metadata including file paths and user information.
* Downloaded assets can provide clues to real-world identities if metadata is present.
* Always use passive OSINT techniques without interacting with the creator or their accounts.
