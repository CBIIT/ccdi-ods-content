---
title: MOCK Format Example
author: data sharing dev team
date: 2025-04-25
---

# Format Examples

This page is used for testing and displaying examples of configurable text on site pages. This formatting can all be edited as a Content Update rather than a full Code Deployment.

## Section 1: Basics

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

### Code Examples

Inline `code` can be written like this.

```python
def hello_world():
    print("Hello, World!")
```

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
[Example Internal Link: This Page](/post/process/MOCK_Format_Example) &#128279;

### Just a line

Above the line

---
Below the line

## Section 2: Images

### Images & Video

Images can be pulled from the web with links:  
![Images should include alt-text too](https://www.cancer.gov/sites/g/files/xnrzdm211/files/ncids_slim_hero/field_slim_hero_image/2025-03/CCDI-Illustrated-MLP-Banner-Design_Final.jpg)

Or custom images can be supported from hosted files: (in-progress)  
![Local upload of folder icon](../images/folder_icon.png)

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

## Section 3: Special characters

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
- Emoji (Unicode): `&#128512;` → 😀, `&#128640;` → 🚀, `&#128221;` → 📝

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
