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
