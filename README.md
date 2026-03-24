# Metro Vested Properties – Static Website

## ⬇️ How to download and deploy

1. In Base44, go to **Code → Files** and download the `static-export` folder
2. Open the downloaded folder — you will see `index.html`, `services.html`, `css/`, `js/`, etc. **at the top level**
3. Create a new GitHub repository (public)
4. Upload **all files and folders from inside `static-export/`** directly to the **root** of the repository (not the folder itself — its contents)
5. Go to **Settings → Pages → Source → Deploy from branch → main → / (root)**
6. Save — your site goes live at `https://yourusername.github.io/repo-name/`

> ✅ No build step. No npm. No configuration. Upload → done.

## File structure (deploy all of these to repo root)

```
index.html          ← Home
services.html       ← Services
about.html          ← About
projects.html       ← Projects / Gallery
reviews.html        ← Reviews
contact.html        ← Contact / Quote form
css/
  style.css         ← All styles
js/
  main.js           ← Navbar, gallery filter, quote form
README.md
```

## Path verification checklist

- ✅ All CSS loaded via `./css/style.css` (relative)
- ✅ All JS loaded via `./js/main.js` (relative)
- ✅ All internal page links use relative filenames (`index.html`, `services.html`, etc.)
- ✅ No absolute paths like `/css/` or `/js/`
- ✅ Works on GitHub Pages project sites (`/repo-name/` subdirectory)

## No build step required

This is a plain static site. No npm, no Node.js, no build system needed.
It works by simply opening `index.html` in a browser or uploading to any static host.

## Dependencies (CDN — internet required to load)

- Google Fonts (Space Grotesk, Inter)
- Font Awesome 6.5 (icons)
- Unsplash (placeholder images — replace with real photos)

## Replacing placeholder images

All gallery and service images currently use Unsplash placeholder URLs.
To replace them, find any `<img src="https://images.unsplash.com/...">` tag and
replace the `src` with a path to your own image file (e.g. `images/kitchen-1.jpg`).

## Removing the gallery

In `projects.html`, the gallery is clearly wrapped in comments:
- `<!-- BEGIN MVP GALLERY -->` ... `<!-- END MVP GALLERY -->`
- `<!-- BEGIN BEFORE/AFTER -->` ... `<!-- END BEFORE/AFTER -->`

Delete everything between those comment pairs to remove the gallery sections.

## Quote form

The quote form on `contact.html` uses a `mailto:` link to open the visitor's
email client with the subject and body pre-filled from their selections.
No backend or third-party service is required.