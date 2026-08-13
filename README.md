# Campus Event Board - IIIT Vadodara

A simple one-page website built with **HTML only** (no CSS, no JavaScript) for a college web development assignment. This README explains *every* line of the code in plain, beginner-friendly language — perfect if this is your very first time working with HTML.

---

## 📁 Files in this project

| File | What it does |
|------|--------------|
| `index.html` | The main web page (the website itself) |
| `logo.png` | The logo image shown at the top of the page |
| `README.md` | This file — the explanation you are reading right now |

---

## 🧠 What is HTML?

**HTML** (HyperText Markup Language) is the skeleton of every website. It uses **tags** — little labels written inside angle brackets like `<h1>` and `<p>` — to tell the browser how to arrange content.

Think of it like building with Lego bricks:

- The **tags** are the bricks.
- You stack them in a certain **order** to build a page.
- A browser reads those bricks and draws the page on your screen.

HTML does **not** handle colors or pretty styling by itself (that's normally CSS's job). This project keeps things simple and clean: it uses basic HTML tags and a few simple *attributes* so that **no CSS file is needed at all**.

---

## 🔍 Reading the code from top to bottom

Here is the code, explained line by line. The line numbers refer to `index.html`.

### Lines 1–7: The document skeleton

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Campus Event Board</title>
  </head>
```

- **`<!doctype html>`** — Tells the browser, "Hey, this is an HTML5 document." Every modern HTML file starts with this line.
- **`<html lang="en">`** — The root tag that wraps *everything* on the page. `lang="en"` says the page is written in English (helps search engines and screen readers).
- **`<head>...</head>`** — The "brain" of the page. Nothing here is shown on screen; it holds *information about* the page.
- **`<meta charset="UTF-8" />`** — Declares the character encoding so that letters, symbols, and emoji display correctly.
- **`<meta name="viewport" ... />`** — Helps the page scale nicely on phones and tablets.
- **`<title>...</title>`** — Sets the text shown in the browser tab (the little label at the top of your browser window).

> 💡 **Note:** The `<head>` content is invisible on the page itself — it only controls tab text, language, and mobile behavior.

### Lines 8–13: The body begins + the logo and page title

```html
<body>
  <center>
    <img src="logo.png" alt="IIIT Vadodara Logo" width="150" height="150" />
    <h1>Campus Event Board</h1>
    <h2>Indian Institute of Information Technology Vadodara</h2>
  </center>
```

- **`<body>`** — Everything visible on the page lives *inside* the body.
- **`<center>...</center>`** — Centers whatever is inside it on the screen. Here it centers the logo and the two headings.
- **`<img src="logo.png" ... />`** — Displays an image (the college logo).
  - `src` → the file name of the image (`logo.png`)
  - `alt` → alternative text shown if the image fails to load (good for accessibility)
  - `width="150"` and `height="150"` → how big the image should be, in pixels (here a 150×150 square)
- **`<h1>...</h1>`** — A level-1 heading. `h1` is the biggest heading and is usually used for the page's main title. Browsers show it large and bold by default.
- **`<h2>...</h2>`** — A level-2 heading. It is smaller than `h1` and is used here for the subtitle (the college name).

> So the top of the page shows the logo, then the main title "Campus Event Board", then the college name as a subtitle — all centered.
### Lines 15–17: The welcome message + first divider

```html
<p>Welcome to the Campus Event Board. Find all the latest events and activities happening on campus.</p>

<hr />
```

- **`<p>...</p>`** — A **p**aragraph. The browser automatically adds some space before and after it.
- **`<hr />`** — A **h**orizontal **r**ule: a straight line across the page that acts as a divider between sections.

### Lines 19–24: The upcoming events list

```html
<h3>Upcoming Events</h3>
<ul>
  <li>Tech Talk: Introduction to AI - Monday, Auditorium</li>
  <li>Coding Hackathon - Friday, CS Block</li>
  <li>Cultural Fest - Saturday, Main Grounds</li>
</ul>
```

- **`<h3>...</h3>`** — A level-3 heading. It is smaller than `h2` and is used here for section titles.
- **`<ul>...</ul>`** — An **u**nordered **l**ist: it shows its items as bullet points.
- **`<li>...</li>`** — A **l**ist **i**tem (one entry inside the list).

> Each `<li>` holds one event, written as: event name - day, venue. This keeps the information short and readable as a simple bullet list.

### Lines 26–32: The contact section

```html
<hr />

<h3>Contact Us</h3>
<p><b>Address:</b> Block No. 9, Government Engineering College, Sector-28, Gandhinagar, Gujarat - 382028</p>
<p><b>Phone:</b> +91-79-29750281</p>
<p><b>Email:</b> <a href="mailto:info@iiitvadodara.ac.in">info@iiitvadodara.ac.in</a></p>
<p><b>Website:</b> <a href="https://iiitvadodara.ac.in">iiitvadodara.ac.in</a></p>
```

- **`<b>...</b>`** — Makes text **bold**. It is used here to make the labels ("Address:", "Phone:", etc.) stand out.
- **`<a href="...">...</a>`** — An **a**nchor: a clickable link.
  - `href` → the destination.
  - `mailto:info@iiitvadodara.ac.in` → an email link. Clicking it opens the user's email app.
  - `https://iiitvadodara.ac.in` → a normal link that opens a website.
  - The text between the tags is what the user sees and clicks.

> So this section shows the college's address, phone number, email, and website as simple lines, with the labels in bold and the email/website as clickable links.

### Lines 34–40: The footer

```html
<hr />

<footer>
  <center>
    <p>&copy; 2026 Campus Event Board, IIIT Vadodara. All rights reserved.</p>
  </center>
</footer>
```

- **`<footer>...</footer>`** — A semantic tag that marks the page's footer (bottom section).
- **`<center>`** — Centers the copyright text.
- **`&copy;`** — The HTML entity that displays the © copyright symbol.

### Lines 41–42: Closing the page

```html
  </body>
</html>
```

- **`</body>`** — Closes the body (everything visible ends here).
- **`</html>`** — Closes the root html tag, marking the very end of the document.
---

## 🧩 Handy "cheat sheet" of tags used in this project

| Tag | Meaning | What it does |
|-----|---------|--------------|
| `<html>` | html root | Wraps the whole document |
| `<head>` | head | Holds page information (not shown) |
| `<title>` | title | Text in the browser tab |
| `<body>` | body | Everything visible on the page |
| `<center>` | center | Centers its contents |
| `<img>` | image | Shows an image |
| `<h1>` | heading 1 | Big main heading |
| `<h2>` | heading 2 | Subheading |
| `<h3>` | heading 3 | Smaller section heading |
| `<p>` | paragraph | A paragraph of text |
| `<hr />` | horizontal rule | Draws a horizontal line |
| `<ul>` | unordered list | Bullet list |
| `<li>` | list item | One item in a list |
| `<b>` | bold | Makes text bold |
| `<a>` | anchor | A clickable link |
| `<footer>` | footer | Marks the bottom of the page |

**A rule to remember:** Most tags come in **pairs** — an opening tag `<tag>` and a closing tag `</tag>` (with a slash). A few are *self-closing* and don't need a closing tag: `<br />`, `<hr />`, `<img />`, `<meta />`.

**Useful attributes used on the image (`<img>`):**
- `src="logo.png"` → which image file to show
- `alt="IIIT Vadodara Logo"` → text shown if the image can't load
- `width="150"` and `height="150"` → the image's size in pixels

---

## 🚀 How to run this project

1. Keep both `index.html` and `logo.png` in the **same folder**.
2. Double-click `index.html`.
3. It will open in your default web browser — done!

You can also right-click `index.html` → **Open with** → choose a browser.

### Troubleshooting

| Problem | Likely cause & fix |
|---------|--------------------|
| Logo doesn't show | `logo.png` is missing from the folder, or the file name/case doesn't match. |
| Page looks plain | That's normal — this version uses no CSS, so it relies on the browser's default styling. |
| Text appears but no image | Check that the `src="logo.png"` value matches the actual file name. |

---

## ✏️ Ideas to practice

- Change the **logo size** by editing `width` and `height` on the `<img>`.
- Add a **new event** with another `<li>...</li>` line in the list.
- Add a **numbered list** with `<ol>` and `<li>` (for steps).
- Change the **copyright year** in the footer.
- Add more **sections** with a new `<h3>` and some `<p>` text.
- Add more **pages** and link them with `<a href="page2.html">`.

---

*Made as part of the Web Development Lab assignment for IIIT Vadodara. Happy coding! 🎓*
