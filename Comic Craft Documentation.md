# 🦸 Comic Story

**A Marvel-Themed Digital Comic Library Website**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-F7DF1E?logo=javascript&logoColor=black)

> Main file: `COMIC_CRAFT_1.html`

---

## Table of Contents

1. [Overview](#1-overview)
2. [Features](#2-features)
3. [Tech Stack](#3-tech-stack)
4. [Project Structure](#4-project-structure)
5. [Getting Started](#5-getting-started)
6. [Page Sections](#6-page-sections)
7. [How It Works](#7-how-it-works)
8. [Customization](#8-customization)
9. [Browser Support](#9-browser-support)
10. [Known Limitations](#10-known-limitations)
11. [Future Improvements](#11-future-improvements)
12. [Conclusion](#12-conclusion)
13. [Disclaimer](#13-disclaimer)

---

## 1. Overview

Comic Story is a front-end portfolio project that presents a curated comic collection through a cinematic, comic-book-inspired interface. It demonstrates responsive layout design, CSS theming with variables, DOM manipulation, client-side search and filtering, modal dialogs, `localStorage` persistence and scroll-based animations.

The entire website lives in a single file, `COMIC_CRAFT_1.html`, with no frameworks, libraries or build tools.

### Why Comic Story?

Comic fans usually scatter their favorite titles across bookmarks, notes and shelves. Comic Story brings them together in one place that feels like opening a real comic book: bold colors, dramatic posters and hero-themed storytelling.

### Project Highlights

- **Immersive superhero experience:** a Marvel-inspired red, blue and gold theme on a dark cinematic background.
- **Complete comic library:** ten iconic titles, from Marvel Comics and Iron Man to Avengers: Endgame and Spider-Man.
- **Instant discovery:** live search and category filters help visitors find a title in seconds.
- **Personal collection:** visitors can save favorite comics, and the choices persist between visits.
- **Cinematic posters:** large featured artwork displays give the site a gallery-style look.
- **Story-driven design:** character cards and "The Journey" timeline tell the story of the universe.
- **Light and dark modes:** visitors pick the viewing style that suits them.
- **Works on every screen:** a responsive layout adapts to phones, tablets and desktops.
- **Fast and lightweight:** one file, no dependencies and no installation.
- **Beginner-friendly code:** clean, well-commented HTML, CSS and JavaScript that is easy to learn from and extend.

### Who Is It For?

| Audience | Value |
| --- | --- |
| **Comic and Marvel fans** | A stylish place to browse and collect favorite stories |
| **Students and learners** | A practical example of a complete front-end project |
| **Recruiters and reviewers** | A portfolio piece showing design and JavaScript skills |
| **Developers** | A ready base to extend with a backend or more content |

### Skills Demonstrated

Responsive Web Design · CSS Variables and Theming · Flexbox and Grid · DOM Manipulation · Event Handling · Search and Filter Logic · Modal Dialogs · localStorage · Intersection Observer · UI/UX Design

---

## 2. Features

- Animated preloader with logo and progress bar
- Fixed, blurred navigation header with smooth-scroll links
- Hero section with call-to-action buttons
- Statistics counters (books, heroes, posters)
- Comic library of 10 titles with live search, category filters (All, Marvel, Avengers, Heroes, Classics) and a "no results" message
- Book detail modal that closes with the X button, an outside click or the `Esc` key
- Favorites system to save or remove titles, remembered between visits
- Toast notifications for user actions
- Poster collection with large cinematic displays
- Character cards with symbol, name and role
- Timeline ("The Journey") with six milestones
- Newsletter signup form with email validation
- Light / dark theme toggle
- Responsive design with a mobile hamburger menu
- Scroll-to-top button and scroll-reveal animations
- Keyboard shortcut: press `/` to jump to the search box

---

## 3. Tech Stack

| Technology | Purpose |
| --- | --- |
| **HTML5** | Semantic page structure |
| **CSS3** | Styling, CSS variables, gradients, animations, media queries |
| **Vanilla JavaScript (ES6)** | Interactivity and logic |
| **Web Storage API (localStorage)** | Saving favorites |
| **Intersection Observer API** | Scroll-reveal animations |

No external libraries, fonts or dependencies are required.

---

## 4. Project Structure

```text
comic-story/
|-- COMIC_CRAFT_1.html    (the complete website: HTML + CSS + JS)
|-- images/               (book covers and posters)
|   |-- MarvelComics.jpg
|   |-- avengers.jpg
|   `-- ...
`-- README.md
```

> **Note:** the HTML file currently references images using local Windows paths. See [Known Limitations](#10-known-limitations) for how to fix this before publishing.

---

## 5. Getting Started

### Run locally

1. Download or clone the project.
2. Put your image files in an `images/` folder next to the HTML file.
3. Double-click `COMIC_CRAFT_1.html` to open it in your browser.

No installation, server or build step is needed.

### Deploy online (free)

- **GitHub Pages:** rename the file to `index.html`, push it to a repository, then enable Pages in the repository settings.
- **Netlify or Vercel:** drag and drop the project folder.

---

## 6. Page Sections

| Section | Description |
| --- | --- |
| **Home (Hero)** | Headline, intro text and buttons leading to the library and posters |
| **Stats** | Summary numbers for the collection |
| **Library** | Searchable, filterable grid of 10 comic titles |
| **Posters** | Two featured poster displays |
| **Story blocks** | Short story texts in a highlighted red section |
| **Characters** | Hero cards: Iron Man, Captain America, Thor, Hulk, Black Widow and more |
| **Timeline** | Marvel Comics, Individual Heroes, The Avengers, Infinity War, Endgame, Spider-Man |
| **About** | Project description with READ / EXPLORE / COLLECT panels |
| **Newsletter** | Email signup form |
| **Footer** | Site links and information |

**Library titles:** Marvel Comics, Iron Man, Captain America, Thor, Hulk, Black Widow, The Avengers, Avengers: Infinity War, Avengers: Endgame, Spider-Man.

---

## 7. How It Works

**Search and filter.** Each book card has `data-title` and `data-category` attributes. The `filterBooks()` function compares every card with the search text and the active filter button, then shows or hides cards to match.

**Detail modal.** Book descriptions are stored in a `comicData` JavaScript object keyed by title. Clicking a card looks up its entry and fills the modal.

**Favorites.** Saved titles are stored as a JSON array in `localStorage` under the key `comicStoryFavorites`, so they persist after refreshing or closing the browser.

**Theme toggle.** The theme button adds or removes a `light-mode` class on the `body` element, and the CSS restyles the page accordingly.

**Animations.** An `IntersectionObserver` fades and slides cards, characters, posters and stats into view as they enter the screen.

---

## 8. Customization

- **Colors:** edit the CSS variables at the top of the style block (`--red`, `--blue`, `--yellow` and so on).
- **Add a book:** copy an existing book-card block, update its `data-title`, `data-category` and `data-book` values, and add a matching entry to the `comicData` object.
- **Change categories:** edit the `data-filter` values on the filter buttons and the `data-category` values on the cards.
- **Change images:** replace files in the `images` folder or update the `src` paths.

---

## 9. Browser Support

Works in current versions of Chrome, Edge, Firefox and Safari. Older browsers without `IntersectionObserver` or `localStorage` support may not display all features.

---

## 10. Known Limitations

- **Image paths:** images currently point to local paths such as `C:\Users\...\MarvelComics.jpg`, so they will not load on other computers or when hosted. Move the images into an `images/` folder and change the paths to relative ones, for example `images/MarvelComics.jpg`.
- **No backend:** the newsletter form does not send data anywhere. Favorites and theme settings exist only in the visitor's own browser.
- **Static content:** all books, characters and timeline entries are written directly in the HTML.

---

## 11. Future Improvements

- [ ] Favorites-only view
- [ ] Sorting options (title, rating)
- [ ] Real newsletter integration
- [ ] Loading book data from a JSON file or API
- [ ] Individual detail pages for each character
- [ ] Separate CSS and JS files for easier maintenance

---

## 12. Conclusion

Comic Story shows that a polished, professional website doesn't need heavy frameworks or complicated tools. With just HTML, CSS and JavaScript, it delivers the things a modern web project should have:

- **A strong visual identity:** a bold, cinematic superhero theme that is instantly memorable.
- **Real interactivity:** search, filters, favorites, modals, notifications and animations that respond to the visitor.
- **Thoughtful user experience:** responsive on all devices, with light and dark modes and keyboard shortcuts.
- **Clean, scalable code:** organized so new comics, characters and features can be added easily.
- **Practical learning value:** a complete example of how front-end pieces fit together in one project.

More than a comic catalog, it is a celebration of the stories and heroes that have inspired generations of readers, presented in a way that fans can explore, enjoy and make their own.

With a backend, user accounts and a larger comic database, Comic Story can grow from a front-end showcase into a full comic platform. Every hero begins with a first chapter, and this project is the first chapter of that story.

---

## 13. Disclaimer

*This is an educational, non-commercial fan project. Marvel, its characters, logos and related artwork are trademarks and copyrights of Marvel Entertainment and their respective owners. No affiliation or endorsement is implied. Replace the artwork with licensed or original content before any public or commercial use.*
