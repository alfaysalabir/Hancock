# 🎮 Hancock – Life Time Gaming Experience

Hancock is a **dark-themed, fully responsive gaming community landing page** built with pure HTML and CSS. It brings tournaments, live streams, a Black Friday game sale, gaming accessories, an elite team showcase, an FAQ and a newsletter footer together on one page.

*Hancock is a single-page gaming website, designed section by section from a gaming template and coded with semantic HTML and BEM-style CSS. It works on mobile, tablet, laptop and desktop screens with no JavaScript and no framework.*

## ✨ Key Features

1. **Hero banner** – bold "LIFE TIME GAMING EXPERIENCE" headline, call-to-action button and social icons over a full-width background image.
2. **Sticky-style navbar** – logo, seven menu links, language, sign-in and search icons. On tablets and phones it turns into a two-row bar with a swipeable menu.
3. **About the community** – feature checklist, highlighted image and four animated counters (112k earning, 12M members, 100k streams, 844 sponsors).
4. **Popular games** – skewed pink showcase panel with character artwork and prev/next buttons.
5. **Live streaming** – three stream cards with play overlays, "LIVE" badges and grayscale-to-colour effect, plus a **Previous Matches** scoreboard with angled team bars.
6. **Black Friday sale** – four game cards with discount badge, old/new price and "+" quick-add icon, followed by the **Games Catalog** banner.
7. **Gaming accessories** – controller, keyboard and monitor cards with price and "ADD TO CART" call to action.
8. **Elite team** – four team cards (Paladins, CS:GO, DOTA 2, Valorant) that switch from grayscale to colour on hover.
9. **FAQ** – four numbered questions in a cross-divider grid that becomes a clean stacked list on small screens.
10. **Footer** – newsletter subscribe bar, quick links, team links, image gallery and copyright line.
11. **Fully responsive** – CSS-only, desktop-first layout tuned for 7 breakpoints (see below).
12. **Accessibility touches** – `prefers-reduced-motion` support turns off the icon animations for people who ask for less motion.

## 📱 Responsive Behaviour

| Breakpoint | Device | What changes |
| --- | --- | --- |
| `> 1400px` | Large desktop | Original design, content centred at 1325px |
| `≤ 1400px` | Laptop | Counters, sale cards and accessories switch to fluid 4-column grids |
| `≤ 1280px` | Small laptop | Catalog and FAQ become fluid, banner underline follows the heading |
| `≤ 1200px` | Tablet landscape | Tighter navbar, fluid games and match sections, 3-column footer |
| `≤ 991px` | Tablet portrait | Two-row navbar with swipeable menu, stacked About and Games, 2-column cards, single-column Team and FAQ, stacked subscribe bar |
| `≤ 767px` | Large phone | Smaller section spacing, stacked match results, single-column streams and accessories |
| `≤ 575px` | Phone | Smaller type, underline below headings, team info below photo, 2-column footer |
| `≤ 480px / 360px` | Small phones | Compact counters, sale grid and nav icons; sale grid becomes one column at 360px |

## 🧰 Technologies Used

| Purpose | Tool |
| --- | --- |
| Markup | HTML5 (semantic sections, `<picture>`, `<nav>`, `<footer>`) |
| Styling | CSS3 – Flexbox, Grid, `clip-path`, `aspect-ratio`, CSS variables, media queries |
| Naming | BEM-style class names (`block__element--modifier`) |
| Icons | [Font Awesome 7](https://fontawesome.com/) (CDN) |
| Fonts | [Oswald](https://fonts.google.com/specimen/Oswald) and [Barlow Condensed](https://fonts.google.com/specimen/Barlow+Condensed) (Google Fonts) |
| JavaScript | None – 100% HTML & CSS |

## 🎨 Design Tokens

All colours and fonts live in `:root` at the top of `Hancock.css`, so the theme is easy to change.

| Variable | Value | Used for |
| --- | --- | --- |
| `--pink_color` | `#FF4655` | Accents, buttons, underlines, hover states |
| `--primary_text_color` | `#FFFFFF` | Headings and body text |
| `--primary_background_color` | `#121212` | Main section background |
| `--secondary_background_color` | `#191919` | Alternate section background |
| `--third_background_color` | `#212121` | Cards and panels |
| `--oswald` | Oswald | Body text, buttons, menu |
| `--barlow_condensed` | Barlow Condensed | Headings and numbers |

## 🚀 Run it locally

No build step is needed.

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/hancock.git
cd hancock

# 2. Open the page
#    Option A: double-click Hancock.html
#    Option B: use a local server (e.g. VS Code "Live Server" or)
npx serve .
```

Then open http://localhost:3000 (or the address your server prints).

> 💡 Test responsiveness by opening Chrome DevTools (`F12`) → **Toggle device toolbar** (`Ctrl + Shift + M`).

## 📁 Folder structure

```
hancock/
├── Hancock.html          # page markup
├── Hancock.css           # styles + responsive layer
├── README.md
└── Images/
    └── Hancock/
        ├── Hancock_Icon.svg          # favicon
        ├── Hancock_Logo.png          # navbar logo
        ├── Hancock_Banner.png        # hero background
        ├── Hancock_About.png
        ├── Hancock_Game_1.png, Hancock_Game_2.png
        ├── Hancock_Stream_1-3.png
        ├── Hancock_Team_1-4.png      # match scoreboard logos
        ├── Hancock_Sale_1-4.png
        ├── Hancock_Catalog_1-5.png
        ├── Hancock_Accesories1-3.png
        ├── Hancock_Elite_Team1-4.png
        └── Hancock_Footer1-6.png     # footer gallery
```

## 🧱 CSS organisation

`Hancock.css` follows the page from top to bottom, one commented block per section:

```
Variables & reset  →  Navbar  →  Banner  →  About  →  Games  →  Streaming & Matches
→  Sale & Catalog  →  Accessories  →  Team  →  FAQ  →  Footer  →  RESPONSIVE LAYER
```

The **responsive layer** sits at the very end of the file and only overrides what must change at each breakpoint, so the desktop design stays untouched.

## ☁️ Deploy

Because this is a static site, you can host it for free:

- **GitHub Pages** – push the repo, then go to *Settings → Pages* and choose the `main` branch. Rename `Hancock.html` to `index.html` so it opens at the root URL.
- **Netlify / Vercel** – drag the project folder in or import the GitHub repo. No build command and no environment variables are needed.
  https://hancock-delta.vercel.app/

> ⚠️ Image paths are **case-sensitive** on most hosts. Make sure file names in `Images/Hancock/` match the names used in `Hancock.html` exactly (for example `Hancock_Logo.png`).

## 🙌 Credits

- Design inspiration: **Themebea** gaming template
- Icons: Font Awesome · Fonts: Google Fonts
- Built as a front-end practice project with HTML & CSS
