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

**Quick open** (double‑click)
- Open `Sun_Down_Frontend/index.html` directly in a modern browser.


### How it works (high level)
- `index.html`: Page layout, loader, sections (`#page1` … `#page5`), Swiper markup, and script/style includes.
- `style.css`: Global reset, responsive rules, animated gradients/blobs, hover overlays, fixed preview image, footer.
- `script.js`:
  - Initializes Locomotive Scroll on `#main`.
  - Sets up hover preview for elements with class `.elem` inside `#elem-container` using their `data-image`.
  - Configures `Swiper` for the carousel.
  - Toggles the mobile menu overlay (`#full-scr`).
  - Fades the loader out after a short delay.






