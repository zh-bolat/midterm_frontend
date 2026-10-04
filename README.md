# Forma — Furniture Store Website

Midterm project for the Frontend course: a multi-page responsive website for
**Forma**, a fictional minimalist furniture store with a showroom in Astana.

The design is inspired by Notion and Apple landing pages: a white background, lots
of whitespace, very large headlines, one blue accent color and rounded cards.

**Live site:** _coming soon_

## Team

| Student | Responsibilities |
|---|---|
| ParasatAshk | Project foundation (shared CSS, navbar, footer), Home page, About page |
| bolatov | Catalog page, Gallery page, Contact page |

## Technologies

- HTML5 (semantic tags: `header`, `nav`, `main`, `section`, `article`, `figure`, `footer`, …)
- CSS3 in one shared file: custom properties, Flexbox, CSS Grid, positioning, media queries
- [Bootstrap 5.3.3](https://getbootstrap.com/) from the jsDelivr CDN (grid, utilities, navbar)
- Google Fonts: Inter and Instrument Serif
- Photos from [Unsplash](https://unsplash.com/)

No build tools and no custom JavaScript — the Bootstrap bundle is only used
for the mobile navbar toggle.

## How to run

1. Download or clone the repository.
2. Open `index.html` in any modern browser.

An internet connection is needed to load Bootstrap and the fonts from their CDNs.

## Folder structure

```
midterm_frontend/
├── index.html       Home
├── about.html       About
├── catalog.html     Catalog   (bolatov)
├── gallery.html     Gallery   (bolatov)
├── contact.html     Contact   (bolatov)
├── css/
│   └── style.css    shared styles for all pages
├── images/          photos used on the pages (.jpg)
└── README.md
```

## Features

### Shared foundation (`css/style.css`)
- Design tokens as CSS custom properties in `:root` (colors, radius, fonts, section spacing)
- Pill-shaped buttons on top of Bootstrap `.btn`: `.btn-accent` (primary) and `.btn-soft` (secondary)
- Headline pill with a dot (`.pill` + `.pill-dot`), like Notion's hero
- Sticky navbar (Bootstrap `navbar-expand-lg` with a collapse menu on small screens)
- Footer with page links and showroom info
- Media queries for two breakpoints: tablet (`max-width: 991.98px`) and mobile (`max-width: 575.98px`)

### Home (`index.html`)
- Hero with a huge headline, pill highlight and two buttons
- Large rounded hero photo with a label chip placed with `position: absolute`
- Room categories in a CSS Grid "bento" layout
- Featured products as cards in a Bootstrap `row` / `col-*` grid
- "Why Forma" feature cards laid out with Flexbox
- Call-to-action band inviting visitors to the showroom

### About (`about.html`)
- Page header (reusable pattern for inner pages)
- Our story: text and photo side by side with the Bootstrap grid
- Numbers row laid out with Flexbox
- Values as a list in a two-column CSS Grid
- Team cards with initials avatars

### Catalog (`catalog.html`)
- Page header with a headline pill
- Six product cards in a Bootstrap `row g-4` grid (`col-12 col-sm-6 col-lg-4`)
- "New" and "Bestseller" tags placed on the cards with `position: absolute`
- Comparison table of all models (`caption`, `thead`, `tbody`, `tfoot`, `th scope`) inside Bootstrap `.table-responsive`
- Call-to-action band linking to Contact and Gallery

### Gallery (`gallery.html`)
- Photo gallery built with CSS Grid: 3 columns, one photo spans two rows and one spans two columns
- Each photo is a `figure` with a `figcaption` chip placed with `position: absolute`
- 2 columns on tablets, 1 column on phones
- Call-to-action band linking to Contact and Catalog

### Contact (`contact.html`)
- "Book a showroom visit" form: name, email, phone (`tel`), date, topic `select`, message `textarea`, consent checkbox
- Every field has a `<label for>`, required fields use `required`; Bootstrap form classes with our own rounded inputs and blue focus ring
- Form and info card side by side with the Bootstrap grid (`col-lg-7` / `col-lg-5`)
- Info card laid out with Flexbox: `address`, opening hours list, `tel:` and `mailto:` links

## Requirements coverage

| Requirement | Where in the code |
|---|---|
| 5+ pages with shared navigation | `index.html`, `about.html`, `catalog.html`, `gallery.html`, `contact.html` — same `header.site-header` and `footer.site-footer` |
| Semantic HTML | `header`, `nav`, `main`, `section`, `article` (product and team cards), `figure`/`figcaption` (hero, story, gallery), `aside` and `address` (Contact), `footer` |
| `div` and `span` | Bootstrap `.container` / `.row` / `.col-*` divs; `.pill`, `.pill-dot`, `.price`, `.product-tag`, `.avatar` spans |
| Table | `catalog.html` `#compare` — `.compare-table` with `caption`, `thead`, `tbody`, `tfoot`, `th scope="col"` / `scope="row"` |
| Form | `contact.html` `#booking` — `.booking-form` with text, email, tel, date, select, textarea, checkbox and labels |
| Flexbox | `.features` (Home), `.stats` (About), `.info-card` and `.hours-list li` (Contact), `.image-chip`, `.brand` |
| CSS Grid | `.category-grid` (Home), `.values-list` (About), `.gallery-grid` (Gallery) |
| Positioning | `.site-header` (`sticky`), `.hero-media` + `.image-chip` (Home), `.product-card` + `.product-tag` (Catalog), `.gallery-item` + `figcaption.image-chip` (Gallery) |
| Bootstrap grid | `#featured` cards (Home), `#story` and `#team` (About), `#products` cards (Catalog), `#booking` (Contact), footer |
| Bootstrap components / utilities | navbar with collapse, `.btn`, `.table`, `.table-responsive`, form classes, `d-flex`, `gap-*`, `mx-auto`, `text-center`, `text-end`, `pt-0`, `mb-*` |
| CSS custom properties | `:root` tokens at the top of `css/style.css` |
| Media queries | end of `css/style.css`: `max-width: 991.98px` (tablet) and `max-width: 575.98px` (mobile) |
| Element, class and ID selectors | `body`, `h1`, `a` … / `.section`, `.btn-accent` … / `#hero`, `#why-forma` |

## Image credits

All photos are from [Unsplash](https://unsplash.com/) and are used under the
[Unsplash License](https://unsplash.com/license). They were resized and cropped
with Unsplash URL parameters.
