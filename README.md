## Sun Down — Animated Frontend Landing Page

An interactive, single‑page frontend inspired by Sundown Studio. It showcases smooth scrolling, animated loaders, a marquee section, hover‑preview gallery, and a carousel — all built with vanilla HTML/CSS/JS plus a few lightweight libraries.

### Folder structure
```
Sun Down/
  └─ Sun_Down_Frontend/
       ├─ index.html
       ├─ style.css
       ├─ script.js
       ├─ icon.png
       ├─ video.mp4
       ├─ NeueHaasDisplayLight.ttf
       ├─ NeueHaasDisplayMediu.ttf
       └─ NeueHaasDisplayRoman.ttf
```

### Features
- **Animated loader**: Sequential headline loader fades in/out before revealing the page.
- **Smooth scrolling**: Powered by `LocomotiveScroll` for a polished scroll experience.
- **Marquee text strip**: Infinite horizontally‑scrolling keywords with a gradient divider.
- **Gooey blob background**: Animated gradient circle adds depth behind content.
- **Hover image preview**: Moving your mouse over list items reveals a fixed preview image.
- **Carousel**: `Swiper` slider configured for centered, auto‑width slides.
- **Responsive navigation**: Desktop links and a mobile menu overlay.
- **Custom typography**: Local Neue Haas Display font files with weights mapped via `@font-face`.

### Tech stack
- **Core**: HTML, CSS, JavaScript 
- **Libraries (CDN)**:
  - Locomotive Scroll
  - Swiper.js

### Getting started
No installation is required. All dependencies load via CDN and local assets.

1) Quick open (double‑click)
- Open `Sun_Down_Frontend/index.html` directly in a modern browser.

2) Recommended: run a lightweight server (avoids any local file policy quirks)
- VS Code Live Server: Right‑click `index.html` → “Open with Live Server”.
- Python (3.x):
```bash
python -m http.server 5500
```
  Then visit `http://localhost:5500/Sun_Down_Frontend/`.

- Node (npx serve):
```bash
npx --yes serve .
```
  Then open the served URL and navigate to `/Sun_Down_Frontend/`.

### How it works (high level)
- `index.html`: Page layout, loader, sections (`#page1` … `#page5`), Swiper markup, and script/style includes.
- `style.css`: Global reset, responsive rules, animated gradients/blobs, hover overlays, fixed preview image, footer.
- `script.js`:
  - Initializes Locomotive Scroll on `#main`.
  - Sets up hover preview for elements with class `.elem` inside `#elem-container` using their `data-image`.
  - Configures `Swiper` for the carousel.
  - Toggles the mobile menu overlay (`#full-scr`).
  - Fades the loader out after a short delay.

### Customization tips
- **Text/content**: Edit copy in `index.html` (e.g., hero headings, marquee words, about section).
- **Work items (hover preview list)**: In `#elem-container`, add another
  ```html
  <div class="elem" data-image="https://example.com/your-image.jpg">
    <div class="overlay"></div>
    <h2>Your Title</h2>
  </div>
  ```
- **Carousel slides**: Replace the placeholder `Swiper` slides inside `.swiper-wrapper`.
- **Colors/brand**: Update theme colors (e.g., orange accents `#FE320A`) in `style.css`.
- **Fonts**: Replace or add `@font-face` sources at the top of `style.css` with your own font files.

### Assets
- Ensure these files remain in `Sun_Down_Frontend/` for paths to resolve:
  - `video.mp4` (hero background video)
  - `icon.png` (favicon)
  - `NeueHaasDisplay*.ttf` (fonts referenced by `style.css`)

### Known notes
- Some browsers restrict certain behaviors when opening files via `file://`. If anything doesn’t animate or preview as expected, use a local server as shown above.

### License
This project is provided as‑is for learning and demonstration purposes. You may adapt it freely; add your preferred license if you plan to distribute.


