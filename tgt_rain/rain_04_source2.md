---
icon: books
---

# rain\_04\_source2

### Challenge Overview

In rain’s second fake article, the author claims to have discovered unpublished information. This claim is suspected to be false.

Your task is to debunk the claim by identifying the original source of the image used in the article. The challenge states that the image originates from an old book that has been digitized, meaning the original source should be publicly accessible.

The final objective is to determine the Digital Object Identifier (DOI) of the true source.

Flag format:

```
SWIMMER{DOI}
```

Example (not the solution):

```
SWIMMER{12.34567/890123}
```

***

### Initial Assumptions

Based on the description and prior challenges involving rain, the following assumptions were made:

* The article would be published on rain’s personal blog linked from their X profile
* The image was likely reused or repurposed from an older publication
* Reverse image search tools could reveal earlier appearances of the image
* Digitized Japanese historical materials often include DOI or NDL identifiers

***

### Investigation Process

#### 1. Locating the Second Fake Article

From rain’s X profile, a link to their blog was found in the bio:

```
brutorain.wordpress.com
```

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 12.36.11 am.png" alt=""><figcaption></figcaption></figure>

Exploring the blog revealed an article referencing “unpublished information”, published on December 21, 2025:

```
https://brutorain.wordpress.com/2025/12/21/誰も知らない真実を発見/
```

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 12.38.38 am.png" alt=""><figcaption></figcaption></figure>

***

#### 2. Analyzing the Blog Post Content

The blog post title translates to:

> “Discover the truth that no one knows”

The caption below the image stated:

> _“I succeeded in obtaining hidden information that no one knew yet. The truth of the world must emerge from the image here.”_

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 12.39.14 am.png" alt=""><figcaption></figcaption></figure>

The post included a single image, which became the main OSINT pivot.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

***

#### 3. Reverse Image Search

The image was extracted and submitted to TinEye for reverse image searching.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 12.39.57 am.png" alt=""><figcaption></figcaption></figure>

One of the results led to the following page:

```
https://epo.wikitrans.net/National_Diet_Building
```

***

#### 4. Identifying the Image Author

On the Wikitrans page, the same image appeared with a caption referencing:

* Fukuzo Watanabe

![](<../.gitbook/assets/Screenshot 2026-01-18 at 12.40.30 am.png>)

The image filename was noted as:

```
National_Diet_Building_Competition_Submission_Watanabe_Fukuzo.jpg
```

***

#### 5. Tracing the Image on Wikimedia Commons

Using the filename as a search query:

```
"National Diet Building Competition Submission Watanabe Fukuzo"
```

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 12.41.15 am.png" alt=""><figcaption></figcaption></figure>

This led to the official Wikimedia Commons file page:

```
https://commons.wikimedia.org/wiki/File:National_Diet_Building_Competition_Submission_Watanabe_Fukuzo.jpg
```

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 12.41.45 am.png" alt=""><figcaption></figcaption></figure>

***

#### 6. Following the Original Source Link

On the Wikimedia Commons page, the File Information section listed a Source link.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 12.42.15 am.png" alt=""><figcaption></figcaption></figure>

The source pointed to the National Diet Library Digital Collection:

```
https://dl.ndl.go.jp/pid/967480/1/7
```

***

#### 7. Identifying the DOI

Opening the NDL page revealed the digitized original document containing the image.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 12.42.49 am.png" alt=""><figcaption></figcaption></figure>

After scrolling down the interface, the following identifier was found:

```
識別子（DOI）
10.11501/967480
```

<figure><img src="../.gitbook/assets/Screenshot 2026-01-18 at 12.43.11 am.png" alt=""><figcaption></figcaption></figure>

***

### Key Findings

* The image used in rain’s article was not unpublished
* It originated from a digitized historical source
* The image was traced through reverse image search and archival references
* The original source includes a valid DOI

***

### Final Flag / Answer

```
SWIMMER{10.11501/967480}
```

***

### Notes & Takeaways

* Reverse image search is essential for debunking claims of exclusivity
* Wikimedia Commons often links directly to primary archival sources
* Digitized historical materials frequently expose DOI or persistent identifiers
* Claims of “unpublished information” can often be disproven through simple OSINT pivots

This challenge highlights how image provenance analysis is a powerful method for fact-checking and debunking misinformation using lawful OSINT techniques.
