# scourge.arw — Photography Portfolio

A curated portfolio of automotive, outdoors, product, and portrait photography by Moaz.

**Live:** https://harmonious-tanuki-23c7da.netlify.app/
**Instagram:** [@scourge.arw](https://instagram.com/scourge.arw)

## Project Structure

```
site/
├── index.html            # Main entry point
├── css/
│   └── styles.css        # All styling
├── js/
│   └── script.js         # App logic, lightbox, navigation
└── assets/
    ├── logo.png          # Brand logo
    └── images/
        ├── automotive/   # 31 automotive photos
        ├── outdoors/     # 17 outdoor/landscape photos
        ├── people/       # 12 portrait photos
        └── products/     # 16 product/still life photos
```

## Local Development

Open a terminal in the `site/` folder and run:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000 in a browser.

## Deployment (Netlify)

1. Go to https://app.netlify.com/drop
2. Drag the entire `site/` folder into the drop zone
3. Wait for deploy to finish

## Adding New Photos

1. Drop the new `.jpeg` into the appropriate folder in `assets/images/`
2. Open `js/script.js`
3. Add a new entry to the relevant `*Imgs` object at the top (e.g. `au32: "assets/images/automotive/au32.jpeg"`)
4. Add a new photo entry to the `photos` array with the correct `img`, `imgSet`, `title`, `loc`, and `cat` values

## Tech

- Vanilla HTML, CSS, and JavaScript — no build step, no dependencies
- Google Fonts (Cormorant Garamond + DM Sans)
- Responsive grid (1 / 2 / 3 columns based on viewport)
- Touch-swipe enabled lightbox with keyboard and arrow-button navigation
