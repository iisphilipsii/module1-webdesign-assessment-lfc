# Liverpool FC Fan Site — Project Explanation

## Structure

The website is a small static site built entirely with HTML and CSS, consisting
of three pages: a **Home** page (`index.html`), a **History** page
(`history.html`), and a **Squad** page (`squad.html`). A single shared
stylesheet, `styles.css`, controls the appearance of all three pages, and a
lightweight SVG image stored in an `images/` folder provides the crest in the
header.

Each page follows the same semantic structure to keep the site consistent and
accessible. A `<header>` holds the crest and site title, followed by a `<nav>`
containing the primary navigation list. The page content sits inside a `<main>`
element, broken into logical `<section>` blocks, and every page ends with a
shared `<footer>` carrying the disclaimer. This repeated skeleton means a
visitor always knows where they are, and the navigation links let them move
freely between the three pages. The site is hosted free of charge using GitHub
Pages, making it publicly accessible at a fixed URL.

## Design choices

The most important decision was to use **semantic HTML** rather than generic
`<div>` elements. Tags such as `<header>`, `<nav>`, `<main>`, `<article>`,
`<section>`, and `<footer>` describe the meaning of each region, which improves
accessibility for screen readers and makes the markup easier to read. A single
`<h1>` per page, with `<h2>` and `<h3>` headings nested logically beneath it,
gives the content a clear hierarchy. Images include descriptive `alt` text,
lists use `<ul>` and `<ol>` appropriately, and tabular data (honours and
players) is presented in proper `<table>` elements with `<caption>`, `<thead>`,
and `scope` attributes on header cells.

For the CSS, I used a Liverpool-inspired palette of red, gold, and teal, defined
as **CSS custom properties** (variables) at the top of the stylesheet. This made
the colour scheme consistent and easy to adjust in one place. I focused on
readability through generous spacing, a comfortable line height, a constrained
content width, and clear typographic contrast. A responsive card grid built with
CSS Grid arranges content into columns that adapt to the screen size, and a
media query stacks the header on narrow displays so the site remains usable on
mobile.

## Challenges

The main challenges were practical rather than purely technical. The first was
using Git correctly: I wanted my opening commit to contain only the homepage and
stylesheet, but I had already committed all five files together. Because it was
the very first (root) commit, the usual `reset HEAD~1` command did not work, and
I had to undo it differently before re-staging only the two files I wanted. This
taught me how staging and commits actually work.

The second challenge concerned the **crest image**. I initially planned to
download the official Liverpool FC badge, but realised it is a registered
trademark and copyrighted, which would be a problem on a publicly published
site. I chose instead to keep a stylised, original placeholder crest, which
keeps the project clear of any intellectual-property issues while still giving
the header a Liverpool identity.

## Improvements

There are several ways the site could be extended. Adding real, properly
licensed photographs would make the pages more engaging, as would extra pages
such as a fixtures list or a stadium guide. The honours and squad data are
currently hard-coded; pulling them from a live source would keep them up to date
automatically. Accessibility could be strengthened further with a "skip to
content" link and tested colour-contrast ratios. Finally, introducing a small
amount of JavaScript — for example, a mobile menu toggle or interactive
elements — would build on the static foundation, though the brief here was
deliberately limited to HTML and CSS.
