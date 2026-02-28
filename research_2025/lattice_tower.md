---
icon: utility-pole-double
---

# lattice\_tower

### Challenge Overview

We are presented with a scenario involving a l**attice tower of a communications facility** that was damaged during an earthquake in Japan in **December 2025**. The objective is to identify the **official technical name** of this facility as a communications hub (its _Shuyokyoku_ or “Accommodation Station” name), which differs from the common name reported in news articles.

***

### Initial Assumptions

1. **News Correlation**: The date “December 2025” implies a specific event. Our first step is to identify the building using relevant news reports.
2.  **Technical Naming Convention**: Japanese telecom facilities, particularly NTT buildings, often have two names:

    * **Branch Name**: Commonly reported in news (e.g., NTT Hachinohe Branch)
    * **Accommodation Station Name**: Internal/technical designation (e.g., Hachinohe NW3 Toukyoku)

    The challenge specifically requires the **Accommodation Station Name**.
3. **OSINT Sources**: Enthusiast blogs, infrastructure databases, and Japanese telecom wikis are ideal for discovering these technical names.

***

### Investigation Process

#### Step 1: Identifying the Event and Building

We searched for reports of an earthquake in **December 2025** that affected communications infrastructure.

* **Event**: A magnitude 7.6 earthquake struck **Aomori Prefecture** on **December 8, 2025**.
* **Damage**: News reports indicated a **70-meter steel lattice tower** atop an **NTT East building in Hachinohe City, Kashiwazaki district**, which was at risk of collapse, prompting evacuations.
* **Common Name in News**: “NTT Aomori Hachinohe Building” (NTT青森八戸ビル) or “NTT East Hachinohe Building.”

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 2.54.33 am.png" alt=""><figcaption></figcaption></figure>

References:

* [Quake-damaged tower forces evacuations in Hachinohe](https://www.asahi.com/ajw/articles/photo/67036034)
* [NTT East steel tower damaged in Aomori earthquake](https://www.japantimes.co.jp/news/2025/12/12/japan/aomori-quake-ntt-tower-damaged/)

***

#### Step 2: Finding the Official Facility Name

With the building identified as the **NTT East Hachinohe Building**, we focused on locating its **technical designation**.

* **Search Queries Used:**
  * NTT八戸ビル 収容局名 (NTT Hachinohe Building Accommodation Station Name)
  * 八戸市柏崎 NTT 鉄塔 (Hachinohe City Kashiwazaki NTT Tower)
* **Discovery**: We located detailed listings in Japanese telecom enthusiast databases that map **NTT buildings to their internal network designations**.
* **Official Technical Name**:
  * Hachinohe NW3 Toukyoku (八戸NW3棟局)
  * The “NW3” likely indicates “Network Center 3” or a similar internal designation.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 3.02.49 am.png" alt=""><figcaption></figcaption></figure>

References:

* [NTT東日本 八戸支店 (八戸NW3棟局)](https://telecom.blog.jp/archives/02_NTTE_Hachinohe.html)

***

### Key Findings

* **Location:** Hachinohe City, Kashiwazaki (Aomori Prefecture).
* **Common Name:** NTT Aomori Hachinohe Building.
* **Official Facility Name:** **八戸NW3棟局** (Hachinohe NW3 Toukyoku).
* **Note:** The "NW3" likely refers to "Network Center 3" or a similar internal designation for that specific building block.

***

### Final Flag / Answer

```
SWIMMER{八戸NW3棟局}
```

***

### Notes & Takeaways

1.  **Distinguish Common vs. Technical Names**:

    The name seen in news reports (e.g., “NTT East Hachinohe Branch”) often differs from the internal network designation used in engineering documents or by enthusiasts (e.g., “Hachinohe NW3”).
2.  **Use of Enthusiast Databases**:

    Japanese infrastructure—trains, telecoms, dams, and towers—often has detailed enthusiast-maintained wikisthat provide technical names and coordinates not found in mainstream media.
3. **Effective OSINT Techniques**:
   * Combine news reports for context (event, date, and location).
   * Use Japanese keywords for precise searches.
   * Reference telecom infrastructure blogs and databases to find internal facility designations.
