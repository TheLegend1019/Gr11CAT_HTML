Got you — sorry about that mess. Here’s a **clean, copy-paste-ready `README.md`** with proper GitHub Markdown. Drop this straight into your repo.

````markdown
# Grade 11 CAT (CAPS/NSC) — HTML From Start to Finish

*A practical, school-friendly guide for building clean, accessible, standards-compliant web pages with **HTML5**. No prior experience required. Use **Notepad++** or any plain-text editor.*

## Table of Contents
1. [What is HTML?](#what-is-html)  
2. [Tools You Need](#tools-you-need)  
3. [Project Folder Setup](#project-folder-setup)  
4. [Your First Page](#your-first-page)  
5. [HTML Page Structure](#html-page-structure)  
6. [Text: Headings, Paragraphs, Emphasis](#text-headings-paragraphs-emphasis)  
7. [Links (Internal, External, Email, Phone)](#links-internal-external-email-phone)  
8. [Images & File Paths](#images--file-paths)  
9. [Lists (ul, ol, dl)](#lists-ul-ol-dl)  
10. [Tables (with headers)](#tables-with-headers)  
11. [Semantic Layout](#semantic-layout-header-nav-main-section-article-aside-footer)  
12. [Forms (inputs, labels, selects, textareas)](#forms-inputs-labels-selects-textareas)  
13. [Media (audio, video, embed)](#media-audio-video-embed)  
14. [Metadata & Favicons](#metadata--favicons)  
15. [Accessibility Essentials (CAPS-aligned)](#accessibility-essentials-caps-aligned)  
16. [Validation & Troubleshooting](#validation--troubleshooting)  
17. [Mini CSS for Neat Marking](#mini-css-for-neat-marking)  
18. [Common Entities & Characters](#common-entities--characters)  
19. [CAPS/NSC Checklist & Rubric Hints](#capsnsc-checklist--rubric-hints)  
20. [Practice Tasks](#practice-tasks)  
21. [Quick Reference Tag Sheet](#quick-reference-tag-sheet)

---

## What is HTML?
**HTML (HyperText Markup Language)** structures content on web pages: headings, paragraphs, images, links, tables, and forms. Browsers read HTML and display it visually.

---

## Tools You Need
- **Plain-text editor:** Notepad++ (Windows), VS Code, or TextEdit (macOS in plain-text mode)  
- **Browser:** Chrome/Edge/Firefox/Safari  
- **Optional:** Image editor to resize/compress pictures (Paint, Photos)

> **Exam tip:** Keep everything **offline** in your project folder so it runs without internet.

---

## Project Folder Setup
```text
Phase3Website/
├─ index.html          (Home)
├─ about.html          (Second page)
├─ results.html        (Third page, e.g., findings/graphs)
├─ assets/
│  ├─ images/
│  │  ├─ logo.png
│  │  └─ pic1.jpg
│  └─ media/
│     └─ clip.mp4
└─ favicon.ico         (optional)
````

**Rules**

* **No spaces** in file names → use `-` or `_`
* Use **relative paths** only (no `C:\...` or `file:///...`)

---

## Your First Page

Create **`index.html`** and paste:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>My Grade 11 CAT Website</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="CAPS Grade 11 CAT website project." />
</head>
<body>
  <h1>Welcome</h1>
  <p>This is my first web page.</p>
</body>
</html>
```

Open it by double-clicking `index.html`.

---

## HTML Page Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Page Title</title>
</head>
<body>
  <!-- Visible content goes here -->
</body>
</html>
```

---

## Text: Headings, Paragraphs, Emphasis

```html
<h1>Main Title (use once)</h1>
<h2>Section Title</h2>
<h3>Subsection</h3>

<p>Paragraph with <strong>important</strong> and <em>emphasised</em> words.</p>
<hr>
```

> **CAPS tip:** Use headings in order (H1 → H2 → H3). Don’t skip levels.

---

## Links (Internal, External, Email, Phone)

```html
<!-- Internal (same site) -->
<a href="about.html">About</a>

<!-- External (new tab) -->
<a href="https://www.gov.za" target="_blank" rel="noopener">South African Government</a>

<!-- Email -->
<a href="mailto:info@example.com">Email Us</a>

<!-- Phone -->
<a href="tel:+27115551234">Call Us</a>

<!-- Jump to section -->
<a href="#contact">Go to Contact</a>
...
<h2 id="contact">Contact</h2>
```

---

## Images & File Paths

```html
<img src="assets/images/logo.png" alt="School logo" width="160" height="160">
```

* **Good `alt` text** describes the image’s purpose.
* **Relative paths:**

  * Same folder: `pic.jpg`
  * Up one folder: `../pic.jpg`
  * Subfolder: `assets/images/pic.jpg`

---

## Lists (ul, ol, dl)

```html
<h3>Unordered (bullets)</h3>
<ul>
  <li>Apples</li>
  <li>Bananas</li>
</ul>

<h3>Ordered (numbers)</h3>
<ol>
  <li>Plan</li>
  <li>Design</li>
  <li>Build</li>
</ol>

<h3>Definition list</h3>
<dl>
  <dt>HTML</dt><dd>Structure of a web page.</dd>
  <dt>CSS</dt><dd>Style and layout.</dd>
</dl>
```

---

## Tables (with headers)

```html
<table>
  <caption>Monthly Sales</caption>
  <thead>
    <tr>
      <th scope="col">Month</th>
      <th scope="col">Units</th>
      <th scope="col">Revenue (R)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">January</th>
      <td>120</td>
      <td>24 000</td>
    </tr>
    <tr>
      <th scope="row">February</th>
      <td>95</td>
      <td>19 000</td>
    </tr>
  </tbody>
</table>
```

> Use `<th>` for headers and include a `<caption>` for accessibility and marking.

---

## Semantic Layout (header, nav, main, section, article, aside, footer)

```html
<header>
  <h1>Eco-Energy Project</h1>
  <p class="tagline">Clean power for smart communities</p>
</header>

<nav>
  <a href="index.html">Home</a> |
  <a href="about.html">About</a> |
  <a href="results.html">Results</a>
</nav>

<main>
  <section>
    <h2>Focus Question</h2>
    <p>How can solar water heaters reduce grid demand in SA schools?</p>
  </section>

  <article>
    <h2>Key Findings</h2>
    <p>Installing SWHs cut peak demand by 18% in winter months.</p>
  </article>

  <aside>
    <h3>Glossary</h3>
    <p><strong>kWh</strong> — Kilowatt-hour, a unit of energy.</p>
  </aside>
</main>

<footer>
  <p>&copy; 2025 Your Name. <a href="mailto:you@example.com">Contact</a></p>
</footer>
```

---

## Forms (inputs, labels, selects, textareas)

```html
<form action="#" method="post">
  <fieldset>
    <legend>Feedback</legend>

    <label for="name">Name</label><br>
    <input id="name" name="name" type="text" required><br><br>

    <label for="email">Email</label><br>
    <input id="email" name="email" type="email" placeholder="you@example.com" required><br><br>

    <label for="topic">Topic</label><br>
    <select id="topic" name="topic">
      <option>General</option>
      <option>Website issue</option>
      <option>Project question</option>
    </select><br><br>

    <label for="msg">Message</label><br>
    <textarea id="msg" name="message" rows="5" cols="30"></textarea><br><br>

    <button type="submit">Send</button>
  </fieldset>
</form>
```

> Always connect `<label>` to its control with `for="id"` for accessibility and easier clicking.

---

## Media (audio, video, embed)

```html
<h3>Audio</h3>
<audio controls>
  <source src="assets/media/theme.mp3" type="audio/mpeg">
  <p>Your browser does not support audio.</p>
</audio>

<h3>Video</h3>
<video controls width="480" poster="assets/images/pic1.jpg">
  <source src="assets/media/clip.mp4" type="video/mp4">
  <p>Your browser does not support video.</p>
</video>
```

> Prefer local files for exams. For YouTube, you may use `<iframe>` only if internet is allowed.

---

## Metadata & Favicons

Add inside `<head>`:

```html
<meta name="author" content="Your Name">
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

---

## Accessibility Essentials (CAPS-aligned)

* Headings in order (`h1` → `h2` → `h3`)
* Meaningful `alt` text for images
* `<label>`s linked to inputs
* Descriptive link text (“Download report (PDF)” not “Click here”)
* Readable contrast & font size

---

## Validation & Troubleshooting

1. Save as **UTF-8** in your editor
2. Validate HTML with **W3C HTML Validator**
3. Fix common errors: unclosed tags, wrong nesting, broken paths

---

## Mini CSS for Neat Marking

Add inside `<head>`:

```html
<style>
  body { font-family: system-ui, Arial, sans-serif; line-height: 1.5; margin: 1.5rem; }
  nav a { margin-right: .75rem; }
  img { max-width: 100%; height: auto; }
  table { border-collapse: collapse; width: 100%; }
  th, td { border: 1px solid #ccc; padding: .5rem; text-align: left; }
  caption { font-weight: 600; margin-bottom: .5rem; }
  footer { margin-top: 2rem; font-size: .9rem; color: #555; }
</style>
```

---

## Common Entities & Characters

* `&nbsp;` — non-breaking space
* `&copy;` — ©
* `&amp;` — &
* `&lt;` — <
* `&gt;` — >

---

## CAPS/NSC Checklist & Rubric Hints

* **Files & Folders:** meaningful names, relative paths, assets subfolders
* **Structure:** valid HTML5, proper `<head>`, logical headings, semantic tags
* **Content:** Home + 2 pages, working nav, topic/focus/abstract, ≥3 findings, table with headers & caption, one form with labels
* **Accessibility:** alt text, labels, descriptive links
* **Quality:** validator passes; consistent spacing and readability

---

## Practice Tasks

* **Task 1 — Hello Web:** Title, heading, two paragraphs, footer
* **Task 2 — Multi-Page Site:** Add `about.html` & `results.html`; create a `<nav>` on all pages
* **Task 3 — Images & Paths:** Add `assets/images/`; show two images with `alt`
* **Task 4 — Tables & Findings:** Table with `<caption>`, `<thead>`, `<tbody>`, row headers
* **Task 5 — Forms:** Name, email, topic (select), message (textarea), submit; all with labels
* **Task 6 — Accessibility Check:** Headings order, alt text, link text
* **Task 7 — Validate & Fix:** Use W3C Validator; correct errors

---

## Quick Reference Tag Sheet

**Document & Structure:** `<!DOCTYPE html>`, `<html lang>`, `<head>`, `<meta charset>`, `<title>`, `<body>`
**Layout:** `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`
**Text:** `<h1>`…`<h6>`, `<p>`, `<strong>`, `<em>`, `<u>`, `<mark>`, `<br>`, `<hr>`
**Links & Media:** `<a>`, `<img>`, `<audio>`, `<video>`, `<source>`, `<iframe>`
**Lists:** `<ul><li>`, `<ol><li>`, `<dl><dt><dd>`
**Tables:** `<table>`, `<caption>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`
**Forms:** `<form>`, `<fieldset>`, `<legend>`, `<label>`, `<input>`, `<select>`, `<option>`, `<textarea>`, `<button>`
**Meta & Icon:** `<meta name="description">`, `<link rel="icon">`

```

Want me to save this into a repo-ready file name (e.g., `Gr11CAT_HTML/README.md`) or tweak the tone/wording for learners?
```
