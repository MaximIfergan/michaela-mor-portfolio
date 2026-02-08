# Project Status - Michaela Mor Portfolio

**Last Updated:** February 8, 2026
**Live Site:** https://maximifergan.github.io/michaela-mor-portfolio/
**Repository:** https://github.com/MaximIfergan/michaela-mor-portfolio

---

## Current State: LIVE

The website is deployed and functional on GitHub Pages.

---

## What's Working

- Home page with hero image (static, no scroll)
- Works page with exhibition folders
- Exhibition pages with lightbox gallery
- About page with CV
- Contact page with email + Instagram
- Fast page transitions (~180ms)
- Mobile responsive design
- Automated exhibition pipeline

---

## Recent Session (Feb 8, 2026)

### Completed

1. **Git Setup & Deployment**
   - Initialized git repository
   - Fixed HTTP 400 push error (increased buffer to 500MB)
   - Deployed to GitHub Pages

2. **Performance Improvements**
   - Reduced page transitions from 1.4s to ~180ms
   - Added `font-display: swap` for instant text rendering

3. **Mobile Fixes**
   - Nav items stay side-by-side (not stacked)
   - Hero image fills screen with `object-fit: cover`
   - Removed gaps on mobile

4. **Home Page**
   - Made static (no scrolling)
   - Equal gaps top/bottom on desktop
   - Full bleed on mobile

5. **About Page**
   - Reduced top gap

6. **Exhibition Pipeline Created**
   - `EXHIBITION_TEMPLATE.md` - Instructions for Michaela
   - `add-exhibition.py` - Automated script:
     - Copies images to correct folder
     - Compresses via ImageMagick
     - Generates exhibition HTML
     - Updates gallery.html

---

## Known Issues / TODO

1. **Desktop hero image** - User noted mobile changes affected desktop. May need adjustment.

2. **Placeholder exhibitions** - exhibition-2, 3, 4 have placeholder content. Remove or populate with real exhibitions.

3. **Cover images missing** - gallery.html references images that don't exist:
   - `images/exhibition-2-cover.jpg`
   - `images/exhibition-3-cover.jpg`
   - `images/exhibition-4-cover.jpg`

---

## How to Continue

### Adding New Exhibitions
```bash
# 1. Get folder from Michaela (images + data.txt)
# 2. Run pipeline
python3 add-exhibition.py ~/path/to/folder/

# 3. Push
git add .
git commit -m "Add exhibition: [Name]"
git push
```

### Making CSS/HTML Changes
```bash
# Edit files, then:
git add .
git commit -m "Description"
git push
# Live in ~1 minute
```

### Testing Mobile
- Chrome: Right-click → Inspect → Device icon (Cmd+Shift+M)
- Safari: Develop → Responsive Design Mode (Cmd+Option+R)

---

## Key Files

| File | Purpose |
|------|---------|
| `index.html` | Home page |
| `gallery.html` | Works listing |
| `exhibition-1.html` | Bezalel Academy (26 images) |
| `about.html` | CV page |
| `contact.html` | Contact info |
| `style.css` | All styles |
| `script.js` | Transitions, lightbox |
| `add-exhibition.py` | Exhibition automation |
| `EXHIBITION_TEMPLATE.md` | Instructions for Michaela |

---

## Technical Reference

### Git Config
```bash
git config http.postBuffer 524288000  # 500MB buffer for large pushes
```

### Image Compression
```bash
# Manual compression (if needed)
./images/compress-images.sh "images/Gallery/[Exhibition Name]"
```
Settings: Max 1920px, 85% quality

### CSS Variables (style.css)
```css
--primary-color: #2c2c2c
--secondary-color: #8b9da8
--text-color: #4a4a4a
--border-color: #f0f0f0
--main-font: 'Sofia Sans', sans-serif
```

### Page Transitions
- Fade-out: 80ms (script.js line 20)
- Fade-in: 100ms (style.css line 62)

---

## Contact Info

- **Artist:** Michaela Mor
- **Email:** michaelasga1998@gmail.com
- **Instagram:** @michaellamor
- **Phone:** 054-3451679

---

*This file tracks project status for continuity between sessions.*
