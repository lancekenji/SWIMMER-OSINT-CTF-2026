---
icon: x-twitter
---

# rain\_01\_social

### Challenge Overview

As of 2026, the individual known as **rain** appears to have had an **X (formerly Twitter)** account. Investigators obtained a **screenshot of a post**, but the username was intentionally obscured by an overlay (appearing like a notepad or masking element).

The task is to **identify the X account** shown in the screenshot and determine the account’s **screen name (ID)**.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

**Flag format:**

```
SWIMMER{@account_name}
```

Example (not the solution):

```
SWIMMER{@gov_online}
```

***

### Initial Assumptions

Based on the provided screenshot and context, the following assumptions were made:

* The UI shown matches **X / Twitter**, based on layout and typography
* Even if the username is hidden, the **post text itself may be searchable**
* X allows searching for **exact text strings**, which can be used as an OSINT pivot
* The language used in the post suggests the account owner may be **Japanese**

***

### Investigation Process

#### 1. Text Extraction from the Screenshot

Despite the username being hidden, the **post content was fully visible** in the screenshot. The readable Japanese text was:

```
これわりと近所だったから見に行ったな
```

This text became the primary OSINT pivot for identifying the account.

***

#### 2. Searching the Text on X

Since the interface appeared to be X, the next step was to perform a **direct search on X** using the extracted text.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 12.20.01 am.png" alt=""><figcaption></figcaption></figure>

By searching the exact Japanese sentence, the platform returned a small number of highly relevant results.

***

#### 3. Identifying the Original Poster

Among the search results, a post was found that **matched the exact text shown in the screenshot**, including formatting and context.

The account that posted the content was identified as:

```
@bruto_rain
```

Visual comparison between the search result and the original screenshot confirmed that the post originated from this account.

***

### Key Findings

* The obscured username could be bypassed by **searching visible post text**
* Exact-text searches on X are effective, especially for non-English content
* The Japanese sentence uniquely identified a single relevant account
* The account responsible for the post is **@bruto\_rain**

***

### Final Flag / Answer

```
SWIMMER{@bruto_rain}
```

***

### Notes & Takeaways

* Text-based OSINT remains powerful even when usernames are intentionally hidden
* Screenshots often leak more information than intended through **searchable content**
* Non-English text can significantly reduce noise during social media investigations
* Platform-native search tools are often sufficient for attribution

This challenge highlights how **content correlation** alone can be enough to deanonymize social media posts using lawful OSINT techniques.
