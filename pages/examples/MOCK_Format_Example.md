---
title: MOCK Format Example
author: data sharing dev team
date: 2025-04-25
---

# Format Examples (MOCK)

This page is used for testing and displaying examples of configurable text on site pages. It is useful for reference during development but will not be included in the final site.

## How it works

The goal of this site is to allow for **rapid content updates**, like changing or adding text-based pages with standard structure.

Each page content is written in [Markdown Language](https://www.markdownguide.org/basic-syntax/) and stored as a `[page_name].md` file within a `[navigation_group]` folder. The navigation bar at the top of the screen can be configured to add/change groups and the pages within. (This file is `Examples/MOCK_Format_Example.md`.)

The website frontend (i.e. what a visitor the site sees) is built as a series of templates that are able to pull the markdown content for each page in real-time. The frontend design takes more time and effort to develop than the markdown content: it involves UI design, writing code, testing the full site (to avoid unexpected, unintented changes), and then a deployment process handled by the CBIIT team.

Changes to content can be rapid (a few days). Changes to the frontend will generally take longer (a few weeks).

### Example: Table of Contents

The Table of Contents on the left side of the screen is part of the frontend template. It will always read the markdown content of a page and automatically fill in the headers. Changing the Table of Contents listed is as simple as changing the markdown (i.e. rapid content update).  
However, moving the Table of Contents to the right side of the screen would require changing the template (i.e. code development and deployment).

## Basics

This is a paragraph with **bold text** and *italic text*. You can also use ***bold and italic*** together.

### Lists

- Bullet list item 1
- Bullet list item 2
  - Nested bullet item 1
  - Nested bullet item 2

1. Ordered list item 1
2. Ordered list item 2
   1. Nested ordered item 1
   2. Nested ordered item 2

### Tables

#### Basic Table

| Header 1 | Header 2 |
|----------|----------|
| Cell 1   | Cell 2   |
| Cell 3   | Cell 4   |

#### Headerless Table

| | |
|---|---|
|Cell 1 | Cell 2 |
|Cell 3 | Cell 4 |

### Links

[Example External Link: GitHub](https://github.com) &#8599;  
[Example Internal Link: This Page](/post/examples/MOCK_Format_Example) &#128279;

### Just a line

Above the line

---
Below the line

### Code

Inline `code` can be written like this.

```python
def hello_world():
    print("Hello, World!")
```

## Images

### Images & Video

Full-size images can be pulled from the web with links:  
![An illustrated banner featuring interconnected scenes: researchers and data scientists with monitors displaying data, supercomputers, and cloud resources on the left and right side of the banner. In the middle of the banner, there are patients (children, adolescents, and young adults), families, pediatric oncologists, and other healthcare professionals.](https://www.cancer.gov/sites/g/files/xnrzdm211/files/ncids_slim_hero/field_slim_hero_image/2025-03/CCDI-Illustrated-MLP-Banner-Design_Final.jpg)

Image max size can be adjusted with html:
<img src="https://www.cancer.gov/sites/g/files/xnrzdm211/files/ncids_slim_hero/field_slim_hero_image/2025-03/CCDI-Illustrated-MLP-Banner-Design_Final.jpg" alt="An illustrated banner featuring interconnected scenes: researchers and data scientists with monitors displaying data, supercomputers, and cloud resources on the left and right side of the banner. In the middle of the banner, there are patients (children, adolescents, and young adults), families, pediatric oncologists, and other healthcare professionals." width="100"/>

Or custom images can be supported from hosted files: (in-progress)  
![Local folder icon. Broken image expected right now.](../images/folder_icon.png)

### Videos

Videos can be embedded using `iframe`.

<iframe
  width="640"
  height="360"
  src="https://nci.rev.vbrick.com/embed?id=a938aa7e-3d6e-4dfa-94b5-18ceae3c179a"
  frameborder="0"
  allowfullscreen
  title="Office of Data Sharing, You, and the Data Sharing Lifecycle">
</iframe>

### Gifs

Existing gifs can be embedded as images with links:

![Spinning protein structure gif](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2c/EF-G%2C_mRNA%2C_and_tRNAs_in_POST_state_PDB_4W29.gif/651px-EF-G%2C_mRNA%2C_and_tRNAs_in_POST_state_PDB_4W29.gif?20180411005001)

## Special characters

### Emojis

- Lightbulb (idea): `&#128161;` → 💡
- Information: `&#8505;` → ℹ️
- Check mark (green): `&#9989;` → ✅
- Alert (warning): `&#9888;` → ⚠️
- Megaphone (announcement): `&#128227;` → 📣
- Exclamation (important): `&#10071;` → ❗
- Question (help): `&#10067;` → ❓
- Star (highlight): `&#11088;` → ⭐
- Book (reference): `&#128218;` → 📖
- Pushpin (note): `&#128204;` → 📌
- Hourglass (in progress): `&#9203;` → ⏳
- Clipboard (task): `&#128203;` → 📋
- Envelope (contact): `&#9993;` → ✉️
- Magnifying glass (search): `&#128269;` → 🔍

### Symbols (with HTML Entities)

- Copyright: `&copy;` → ©
- Registered: `&reg;` → ®
- Trademark: `&trade;` → ™
- Degree: `&deg;` → °
- Plus-minus: `&plusmn;` → ±
- Arrow right: `&rarr;` → →
- Arrow left: `&larr;` → ←
- Arrow up: `&uarr;` → ↑
- Arrow down: `&darr;` → ↓
- Check mark: `&#10003;` → ✓

### Non-standard Characters (with HTML Entities)

- Accented: `&eacute;` → é, `&uuml;` → ü, `&ntilde;` → ñ, `&aring;` → å, `&ccedil;` → ç
- Greek: `&alpha;` → α, `&beta;` → β, `&gamma;` → γ, `&delta;` → δ, `&Omega;` → Ω
- Cyrillic (Unicode): `&#1044;` → Д, `&#1046;` → Ж, `&#1071;` → Я

#### Right-to-left text

> مثال على نص باللغة العربية  
> דוגמה לטקסט בעברית

#### Combining Characters (with Unicode)

- a + ́: `a&#769;` → á
- o + ̈: `o&#776;` → ö
- n + ̃: `n&#771;` → ñ
- e + ̊: `e&#730;` → e̊
- s + ̩: `s&#809;` → s̩
- z + ̇: `z&#775;` → ż

## Callouts

### Blocks

> **Note:**  
> Blockquotes can be used to highlight important information, tips, or warnings.
---
> **&#9888; Note:**  
> &#10071; Add emojis for extra emphasis.

### Collapsible Sections

<details>
  <summary>&#128161; Click to expand for more info</summary>
    &#8505; This content is hidden until the user clicks the summary above.  
    Useful for FAQs or advanced details. <br> Requires some html.
</details>

&nbsp;  

---

**Updated:** June 3, 2025
