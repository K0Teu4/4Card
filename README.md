# Frontend Mentor - Four card feature section solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-WKk_WGq8a). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### Screenshot

![Four Card Feature Section](./preview.jpg)

### Links

- Solution URL: [GitHub Repository](https://github.com/K0Teu4/4Card)
- Live Site URL: [GitHub Pages](https://k0teu4.github.io/4Card/)

## My process

### Built with

- Semantic HTML5 markup (header, section, article, h1/h2 hierarchy)
- CSS Grid with a staggered desktop layout
- Per-card accent color via a CSS custom property
- Mobile-first workflow
- Google Fonts (Poppins, weights 200 / 400 / 600)

### What I learned

This challenge is all about multi-column responsive layouts.

#### Staggered grid on desktop
The design places Supervisor and Calculator vertically centered at the sides, while Team Builder and Karma stack in the middle column. I achieved this with a 3-column grid where the side cards span both rows (grid-row: 1 / 3) and use align-self: center, while the middle cards occupy rows 1 and 2. On mobile everything collapses to a single column in DOM order.

#### One rule for four accent colors
Instead of writing four border-top rules, each modifier class sets a custom property (for example --accent: var(--cyan)) and the base card rule consumes it: border-top: 4px solid var(--accent). Adding a fifth card later would take one line.

#### Decorative images and accessibility
The four icons are purely decorative, so they carry an empty alt attribute and aria-hidden="true" — screen readers skip them and the card text stays the single source of meaning.

#### Fluid heading
The intro heading uses clamp() so the two-line title (light 200 + bold 600) scales smoothly between mobile and desktop without media queries.

### Useful resources

- [MDN — CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout)
- [MDN — grid-row](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-row)
- [MDN — Using custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [web.dev — Learn CSS](https://web.dev/learn/css)

## Author

- GitHub — [@K0Teu4](https://github.com/K0Teu4)
- Frontend Mentor — [@K0Teu4](https://www.frontendmentor.io/profile/K0Teu4)
