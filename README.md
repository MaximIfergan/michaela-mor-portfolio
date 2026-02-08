# Michaela Mor - Portfolio Website

A clean, minimal portfolio website for artist Michaela Mor.

**Live Site:** https://maximifergan.github.io/michaela-mor-portfolio/

## Quick Start

### Adding a New Exhibition

1. **Get files from Michaela** - folder with images + filled template (see `EXHIBITION_TEMPLATE.md`)

2. **Run the pipeline:**
   ```bash
   python3 add-exhibition.py ~/path/to/exhibition_folder/
   ```

3. **Push to live:**
   ```bash
   git add .
   git commit -m "Add exhibition: [Name]"
   git push
   ```

That's it! The script handles copying, compressing, and generating HTML.

### Prerequisites

- **Python 3** (comes with macOS)
- **ImageMagick** for image compression:
  ```bash
  brew install imagemagick
  ```

## Project Structure

```
michaela_website/
├── index.html              # Home page (static, no scroll)
├── gallery.html            # Works page with exhibition folders
├── exhibition-1.html       # Bezalel Academy (26 images)
├── exhibition-2/3/4.html   # Additional exhibitions
├── about.html              # CV/bio page
├── contact.html            # Contact info + Instagram
├── style.css               # All styles (Sofia Sans font)
├── script.js               # Page transitions, lightbox
│
├── add-exhibition.py       # Automated exhibition pipeline
├── EXHIBITION_TEMPLATE.md  # Instructions for Michaela
│
├── images/
│   ├── home_page.jpg
│   ├── Gallery/
│   │   └── [Exhibition Name]/  # Exhibition images
│   └── compress-images.sh      # Image compression script
│
└── fonts/                  # Sofia Sans, Kumbh Sans, Julius Sans One
```

## Customization

### Colors
Edit CSS variables in `style.css`:
```css
:root {
    --primary-color: #2c2c2c;
    --secondary-color: #8b9da8;
    --text-color: #4a4a4a;
    --border-color: #f0f0f0;
}
```

### Fonts
Change font in `style.css` lines 40-42:
```css
--main-font: 'Sofia Sans', sans-serif;
--body-font: 'Sofia Sans', sans-serif;
```
Available: Sofia Sans, Kumbh Sans, Julius Sans One

### Page Transitions
Current: ~180ms total (80ms fade-out + 100ms fade-in)
Edit in `style.css` and `script.js`

## Deployment

Site is hosted on **GitHub Pages** (free).

**To update the live site:**
```bash
git add .
git commit -m "Description of changes"
git push
```
Changes appear within 1-2 minutes.

**Repository:** https://github.com/MaximIfergan/michaela-mor-portfolio

## Technical Notes

- **Git push buffer:** Set to 500MB (`git config http.postBuffer 524288000`) to handle image uploads
- **Image compression:** Max 1920px, 85% quality via `compress-images.sh`
- **Mobile:** Hero image uses `object-fit: cover` to fill viewport
- **Fonts:** Use `font-display: swap` for fast loading

## Contact

- **Artist:** Michaela Mor
- **Email:** michaelasga1998@gmail.com
- **Instagram:** [@michaellamor](https://www.instagram.com/michaellamor/)
