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

HTML does **not** care about colors or pretty styling by itself (that's normally CSS's job). This project, however, styles everything using older HTML *attributes* so that **no CSS file is needed at all**.

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
    <title>Campus Event Board - IIIT Vadodara</title>
  </head>
```

- **`<!doctype html>`** — Tells the browser, "Hey, this is an HTML5 document." Every modern HTML file starts with this line.
- **`<html lang="en">`** — The root tag that wraps *everything* on the page. `lang="en"` says the page is written in English (helps search engines and screen readers).
- **`<head>...</head>`** — The "brain" of the page. Nothing here is shown on screen; it holds *information about* the page.
- **`<meta charset="UTF-8" />`** — Declares the character encoding so that letters, symbols, and emoji display correctly.
- **`<meta name="viewport" ... />`** — Helps the page scale nicely on phones and tablets.
- **`<title>...</title>`** — Sets the text shown in the browser tab (the little label at the top of your browser window).

> 💡 **Note:** The `<head>` content is invisible on the page itself — it only controls tab text, language, and mobile behavior.

### Lines 8–20: The body begins + the logo and main heading

```html
<body text="#3d3d3d" link="#1a5276" vlink="#6c3483" alink="#e74c3c">
  <center>
    <img src="logo.png" alt="IIIT Vadodara Logo" width="130" height="130" />
    <br /><br />
    <font face="Georgia, serif" size="7" color="#1a5276">
      <b>Campus Event Board</b>
    </font>
    <br />
    <font face="Arial, sans-serif" size="4" color="#8e6f1e">
      <i>Indian Institute of Information Technology Vadodara</i>
    </font>
  </center>
```

- **`<body ...>`** — Everything visible on the page lives *inside* the body. Its attributes set default colors:
  - `text` → normal text color (dark grey)
  - `link` → color of clickable links
  - `vlink` → color of **v**isited links
  - `alink` → color of **a**ctive (currently clicked) links
- **`<center>...</center>`** — Centers whatever is inside it on the screen.
- **`<img src="logo.png" ... />`** — Displays an image.
  - `src` → the file name of the image (`logo.png`)
  - `alt` → alternative text shown if the image fails to load (good for accessibility)
  - `width` / `height` → how big the image should be (130×130 pixels)
- **`<br />`** — A line **br**eak. It moves the next content to a new line (like pressing Enter).
- **`<font face="..." size="..." color="...">`** — Styles text:
  - `face` → the font family (e.g., Georgia, Arial)
  - `size` → how big (1 = small, 7 = biggest)
  - `color` → the text color (in hex, like `#1a5276`)
- **`<b>...</b>`** — Makes text **bold**.
- **`<i>...</i>`** — Makes text *italic*.

> So the top of the page shows the logo, then a big bold title "Campus Event Board", then a smaller italic subtitle with the college name.

### Lines 22–29: The scrolling marquee banner

```html
<marquee bgcolor="#e8d59a" behavior="scroll" direction="left" scrollamount="6">
  <font face="Verdana, sans-serif" size="3" color="#7d6608">
    <b>
      Welcome to the Campus Event Board! ... &nbsp;|&nbsp; ...
    </b>
  </font>
</marquee>
```

- **`<marquee>...</marquee>`** — Creates a scrolling text banner (a fun, old-school HTML feature).
  - `bgcolor` → background color of the banner
  - `direction="left"` → text moves leftward
  - `scrollamount="6"` → how fast it scrolls
- **`&nbsp;`** — The HTML code for a **non-breaking space** (a space that can't be split across lines). Used here to add spacing around the `|` separator.
- **`|`** — A plain vertical bar used as a visual separator between announcements.

### Lines 31–39: First divider + "Upcoming Events" heading

```html
<center>
  <hr width="70%" color="#1a5276" size="3" />
</center>

<center>
  <font face="Arial, sans-serif" size="5" color="#1a5276">
    <b><u>Upcoming Events</u></b>
  </font>
</center>
```

- **`<hr />`** — A **h**orizontal **r**ule (a straight line across the page).
  - `width="70%"` → the line spans 70% of the page
  - `color` → the line's color
  - `size` → the line's thickness
- **`<u>...</u>`** — Underlines the text.
- So this section draws a decorative line, then shows a big underlined "Upcoming Events" heading.

### Lines 41–69: The events table

```html
<table border="2" bordercolor="#1a5276" cellpadding="8" cellspacing="0" width="80%" bgcolor="#ffffff">
  <tr bgcolor="#1a5276">
    <th>...</th>  <!-- column headers -->
  </tr>
  <tr>
    <td>...</td>  <!-- row 1 data -->
  </tr>
  ...
</table>
```

A **table** is a grid of rows and columns, perfect for listing events neatly.

- **`<table ...>`** — Creates the table. Its attributes:
  - `border="2"` → thickness of the table border
  - `bordercolor` → border color
  - `cellpadding="8"` → space *inside* each cell around the text
  - `cellspacing="0"` → space *between* cells (0 = no gap)
  - `width="80%"` → the table takes up 80% of the page
  - `bgcolor` → background color of the table
- **`<tr>...</tr>`** — A **t**able **r**ow (one horizontal line of cells).
- **`<th>...</th>`** — A **t**able **h**eader cell. Text here is bold and centered by default. Used for the column titles: **Event**, **Day & Time**, **Venue**.
- **`<td>...</td>`** — A **t**able **d**ata cell. Holds one piece of information, like "Coding Hackathon".

> Rows with `bgcolor="#f1e9cd"` (a light cream) alternate with white rows. This "zebra striping" makes the table easier to read, even without CSS.

### Lines 71–86: "How to Register" ordered list

```html
<font face="Arial, sans-serif" size="3">
  <center>
    <b><font size="4" color="#1a5276">How to Register</font></b><br />
    <ol align="left">
      <li>Pick an event from the list above.</li>
      <li>Visit the Student Activities Office to register.</li>
      <li>Collect your event pass on the day of the event.</li>
    </ol>
  </center>
</font>
```

- **`<ol>...</ol>`** — An **o**rdered **l**ist: it shows items numbered 1, 2, 3 automatically.
- **`<li>...</li>`** — A **l**ist **i**tem (one entry inside the list).
- **`align="left"`** — Lines the numbers/text to the left inside the centered block.

> `ol` gives numbers; `ul` (unordered list) would give bullet points instead. This project uses `ol` here because the steps should be in order.

### Lines 88–131: The 3-column section (About / Contact / Quick Links)

```html
<table border="0" width="80%" cellpadding="6" cellspacing="0">
  <tr>
    <td align="center" bgcolor="#1a5276" width="33%">About IIIT Vadodara</td>
    <td align="center" bgcolor="#1a5276" width="33%">Contact Us</td>
    <td align="center" bgcolor="#1a5276" width="34%">Quick Links</td>
  </tr>
  <tr>
    <td valign="top" bgcolor="#ffffff"> ...info... </td>
    <td valign="top" bgcolor="#ffffff"> ...contact info... </td>
    <td valign="top" bgcolor="#ffffff"> ...links... </td>
  </tr>
</table>
```

- This table has **2 rows** and **3 columns**.
  - Row 1 = the three dark blue **column titles**.
  - Row 2 = the actual **content** under each title.
- **`align="center"`** → centers the text inside a cell.
- **`valign="top"`** → **v**ertical **align** to the top, so text starts at the top of each cell.
- **`width="33%"` / `"34%"`** → each column takes roughly one-third of the table.
- Inside the Contact cell, notice the **links**:
  - `<a href="mailto:info@iiitvadodara.ac.in">` → an email link. Clicking it opens the user's email app.
  - `<a href="https://iiitvadodara.ac.in">` → a normal link to a website. The `href` holds the destination; the text between the tags is what the user clicks.

### Lines 137–147: "About Us" paragraph

```html
<font face="Arial, sans-serif" size="3">
  <center>
    <b><font size="4" color="#1a5276">About Us</font></b>
    <p>
      The Campus Event Board is run by the Student Council of IIIT Vadodara ...
      <a href="mailto:events@iiitvadodara.ac.in">events@iiitvadodara.ac.in</a>.
    </p>
  </center>
</font>
```

- **`<p>...</p>`** — A **p**aragraph. The browser automatically adds some space before and after it.
- This section is a simple paragraph describing who runs the site.

### Lines 149–167: The footer

```html
<hr width="100%" color="#1a5276" size="3" />

<center>
  <font face="Georgia, serif" size="3" color="#1a5276">
    <b>Campus Event Board - IIIT Vadodara</b>
  </font>
  <br />
  <font face="Arial, sans-serif" size="2" color="#5a5a5a">
    Indian Institute of Information Technology Vadodara<br />
    c/o Block No. 9, Government Engineering College, Sector-28,<br />
    Gandhinagar, Gujarat - 382028, India<br />
    Phone: +91 79-XXXX-XXXX &nbsp;|&nbsp; Email: <a href="mailto:info@iiitvadodara.ac.in">info@iiitvadodara.ac.in</a><br />
    Website: <a href="https://iiitvadodara.ac.in">iiitvadodara.ac.in</a>
  </font>
  <br /><br />
  <font face="Arial, sans-serif" size="2" color="#8b0000">
    <b>&copy; 2026 Campus Event Board, IIIT Vadodara. All rights reserved.</b>
  </font>
</center>
```

- A full-width `<hr>` separates the footer from the rest of the page.
- **`&copy;`** — The HTML entity that displays the © copyright symbol.
- The footer repeats the college's full address, phone, email, and website — exactly like a typical website footer.

### Lines 169–170: Closing the page

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
| `<br />` | break | Moves to a new line |
| `<font>` | font | Styles text (size, color, font) |
| `<b>` | bold | Makes text bold |
| `<i>` | italic | Makes text italic |
| `<u>` | underline | Underlines text |
| `<marquee>` | marquee | Makes text scroll |
| `<hr />` | horizontal rule | Draws a horizontal line |
| `<table>` | table | Creates a table grid |
| `<tr>` | table row | A row in a table |
| `<th>` | table header | A header cell |
| `<td>` | table data | A normal data cell |
| `<ol>` | ordered list | Numbered list |
| `<ul>` | unordered list | Bullet list |
| `<li>` | list item | One item in a list |
| `<p>` | paragraph | A paragraph of text |
| `<a>` | anchor | A clickable link |

**A rule to remember:** Most tags come in **pairs** — an opening tag `<tag>` and a closing tag `</tag>` (with a slash). A few are *self-closing* and don't need a closing tag: `<br />`, `<hr />`, `<img />`, `<meta />`.

---

## 🎨 How is this styled without CSS?

Normal modern websites use a separate CSS file for colors and layout. This project deliberately avoids CSS for the assignment, so it uses **older HTML attributes** instead:

- `bgcolor="..."` → background color
- `text="..."`, `color="..."` → text color
- `font face` → font family
- `font size` → text size
- `width`, `height` → sizes of elements/images
- `border`, `cellpadding`, `cellspacing` → table appearance

These attributes are mostly outdated (CSS is the proper modern way), but they are perfect for learning the fundamentals and are widely accepted in beginner HTML assignments.

> ⚠️ **Heads up:** `<center>`, `<font>`, and `<marquee>` are considered *deprecated* in modern HTML. They still work in browsers, but teachers and professionals will usually tell you to prefer CSS. For a learning assignment, they're fine!

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
| Page looks plain / no colors | You might have opened a *different* file, or the browser cached an old version (press `Ctrl + F5`). |
| Text appears but no styling | Make sure `index.html` is the exact file in this folder. |

---

## ✏️ Ideas to practice

- Change the **colors** (edit the hex values like `#1a5276`).
- Add a **new event row** by copying a `<tr>...</tr>` block in the table.
- Add a **bullet list** with `<ul>` and `<li>`.
- Change the **marquee speed** by editing `scrollamount`.
- Add more **pages** and link them with `<a href="page2.html">`.

---

*Made as part of the Web Development Lab assignment for IIIT Vadodara. Happy coding! 🎓*
