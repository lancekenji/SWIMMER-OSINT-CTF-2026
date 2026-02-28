# dabeyohiru\_05\_hidden1

#### Challenge Overview

The task is to determine the **legal name** of the user `debeyohiru/furaigo5`. We are given access to their public profile page and are instructed to identify the real name in Latin alphabet, ignoring Kanji or Hiragana.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 3.09.13 am.png" alt=""><figcaption></figcaption></figure>

***

#### Initial Assumptions

1. **Public Source Only**: We cannot contact the user directly or access private accounts. Only lawful OSINT methods are allowed.
2. **Metadata Clues**: Usernames, profiles, and website scripts often contain author or creator metadata.
3. **File References**: JavaScript or HTML source files are potential sources of author information.

***

#### Investigation Process

**Step 1: Inspect the Profile Source**

* Visited `https://furaigo5.github.io/profile/index.html`.
* Explored the page structure and located the linked JavaScript file: `/js/script.js`.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 3.09.51 am.png" alt=""><figcaption></figcaption></figure>

**Step 2: Examine the JavaScript File**

* Opened `/js/script.js` and checked the **header comments**.
* Found the **author** **metadata** clearly stated:

```
/**
 * @fileoverview furaigo5 Workspace - メインスクリプト
 * ナビゲーションのスムーズスクロールとモバイルメニューの制御を担当
 * @author Gotanno Tsubasa
 */
```

* The `@author` tag reveals the user’s real name.
* ![](<../.gitbook/assets/Screenshot 2026-01-18 at 3.10.19 am.png>)

***

#### Key Findings

* **Source**: /js/script.js linked from profile
* **Author / Real Name**: Gotanno Tsubasa

***

#### Final Flag / Answer

```
SWIMMER{Gotanno Tsubasa}
```

***

#### Notes & Takeaways

* **Check Source Files**: Even when profiles appear anonymous, author metadata in scripts, HTML, or CSS can reveal real names.
* **OSINT Principle**: Always start with publicly available sources and inspect client-side files before attempting deeper investigation.
