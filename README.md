# Native English Academy – Website

A one-page website for **Native English Academy**, an official Cambridge exam preparation centre in Molina de Segura, Murcia. The site presents the academy, explains the Cambridge exam levels it prepares students for (B1, B2 and C1), invites teachers to send their CV, and gives contact details and an information request form.

This was one of my first projects in **1º DAM (Desarrollo de Aplicaciones Multiplataforma, FP Grado Superior)**, for the subject **Lenguajes de Marcas y Sistemas de Gestión de Información**. The aim was to build a complete web page using only **HTML and CSS**.

**Author:** [Your name]
**Course:** 1º DAM – Lenguajes de Marcas
**Date:** [Date]

---

## How to view it

1. Put all the files together in one folder (see the folder structure below).
2. Open `Academianative.html` in any modern web browser.

There is nothing to install and no JavaScript. An internet connection is only needed for the hero background photo and the external links.

---

## Folder structure

```
native-academy/
├── Academianative.html   The web page (structure and content)
├── style.css             All the styles (colours, layout, responsive design)
├── Logo Native.png       Academy logo in the navigation bar
├── peoplestudyphoto.png  Gallery photo: students studying
├── cambridgephoto.png    Gallery photo: Cambridge badge
├── badgeukphoto.png      Gallery photo: UK badge
└── teamwork.png          Photo in the "Trabaja con nosotros" section
```

The HTML holds the content and the CSS holds the design, so the look of the page can be changed without touching the content.

---

## Page sections

The whole site is a single page. The menu links jump to each section using anchors (`href="#examenes"` goes to the element with `id="examenes"`).

| Section | What it shows |
|---|---|
| **Navigation bar** | The logo and the menu: *Sobre nosotros*, *Trabaja con nosotros*, *Prueba de nivel* and *Exámenes*. It stays fixed at the top while scrolling. |
| **Hero** | The main title *"Aprendizaje, Certificación y Fluidez"* over a blue-tinted photo, with links to the location on Google Maps and to Cambridge resources. |
| **Sobre nosotros** | A gallery of three photo cards: dedicated learning, official preparation centre and certification. |
| **Exámenes** | Three boxes explaining why the **B1 Preliminary**, **B2 First** and **C1 Advanced** levels are important. |
| **Trabaja con nosotros** | A photo and a button that opens the user's email program to send a CV (`mailto:` link). |
| **Contacto** | Address, email, phone number and a link to Google Maps. |
| **Infórmate** | A form asking for name, level, message, phone and email. |
| **Footer** | Copyright notice. |

The *Prueba de nivel* link takes the user to the official Cambridge online level test, and opens in a new tab (`target="_blank"`) so the academy's page stays open.

---

## HTML features used

- **Semantic elements:** `<nav>`, `<header>`, `<section>` and `<footer>` describe what each part of the page is.
- **Lists for the menu:** the menu links are inside a `<ul>`, which is the standard way to mark up navigation.
- **Internal anchors:** `id` attributes and `#` links for one-page navigation.
- **External links:** Google Maps, Cambridge English and the level test, opened in a new tab.
- **`mailto:` link:** opens a new email to the academy.
- **Images with `alt` text:** describes each image for screen readers and if the image fails to load.
- **Forms:** text, telephone (`type="tel"`) and email (`type="email"`) inputs, a dropdown (`<select>`), the `required` attribute, and placeholders.
- **Page settings:** `lang="es"`, `charset="UTF-8"` (for accents and ñ) and the `viewport` meta tag for mobile screens.

---

## CSS features used

- **CSS variables:** the academy's colours are defined once in `:root` (navy `#00247d`, red `#cf142b`, white and light grey), inspired by the British flag. Changing a colour there updates the whole page.
- **Sticky navigation bar:** `position: sticky` keeps the menu visible while scrolling.
- **Smooth scrolling:** `scroll-behavior: smooth` makes menu links glide to their section, and `scroll-margin-top` stops the sticky bar from covering the section titles.
- **Hero background:** a `linear-gradient` laid over a photo gives the blue tint and keeps the white text readable.
- **CSS Grid:** the photo gallery uses `repeat(auto-fit, minmax(300px, 1fr))`, so the cards rearrange automatically to fit the screen.
- **Flexbox:** used for the navigation bar, the exam boxes, the "Trabaja con nosotros" section and the phone/email row of the form.
- **`object-fit: cover`:** keeps the gallery photos the same height without stretching them.
- **Hover effects and transitions:** menu links, buttons and exam boxes change colour or gain a shadow smoothly when the mouse is over them.

---

## Responsive design

The page adapts to different screen sizes using media queries:

- **768px or narrower (tablets and phones):** the exam boxes and the "Trabaja con nosotros" section stack vertically instead of sitting side by side.
- **480px or narrower (small phones):** the phone and email fields in the form stack on top of each other.
- The gallery adjusts on its own at any width thanks to Grid's `auto-fit`.

---

## Limitations and future improvements

This was an early project, so there are things I would improve now:

- **The form doesn't send anything yet.** It has no `action` and there is no server, so it only shows how the form would look. It would need a back end or a form service to work.
- The nav menu doesn't collapse into a "hamburger" menu on phones.
- The hero background image is loaded from Unsplash, so it needs an internet connection. It could be downloaded into the project folder instead.
- Rename `Academianative.html` to `index.html` so it opens automatically when published online (for example on GitHub Pages).
- Avoid spaces in file names (`Logo Native.png` → `logo-native.png`), which can cause problems on some web servers.
- Write the `alt` texts in Spanish to match the page language.
- Validate the page with the [W3C Markup Validation Service](https://validator.w3.org/).

---

## Credits

- **Hero background photo:** [Unsplash](https://unsplash.com/).
- **Exam information and level test:** [Cambridge English](https://www.cambridgeenglish.org/).
- **Other images:** [Add the source of the logo and the gallery photos here]
