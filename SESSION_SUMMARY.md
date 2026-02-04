# Session Summary - Michaela Mor Portfolio Website
**Date:** February 3, 2026

---

## Project Overview

Created a complete portfolio website for artist Michaela Mor with:
- Clean, minimal design
- Custom fonts
- Gallery system with exhibition folders
- Full CV integration
- Smooth page transitions
- Mobile responsive

**Live Goal:** Deploy to GitHub Pages (in progress - deployment issue to resolve)

---

## Iterations & Changes Made

### Initial Setup (Iteration 1)
- Created basic HTML/CSS/JS structure
- 4 pages: Home, Gallery, About, Contact
- Gallery with lightbox functionality
- Clean minimal design inspired by tamirchen.com and daniel-oksenberg.com

### Iteration 2 - Simplification
**Removed:**
- Featured Work section from home page
- Contact form ("Send a Message")
- Copyright footer banner

**Changed:**
- Gallery restructured into "exhibition folders" system
- Each exhibition has its own page with artwork galleries
- Created 4 exhibition templates
- Contact page simplified to email, location, social links only

**Styling:**
- Made borders very subtle (#f0f0f0)
- Muted colors (#8b9da8)
- Transparent footer

### Iteration 3 - Content & Bezalel Exhibition
**Gallery System:**
- Exhibition-1 populated with 26 images from "Bezalel Academy" folder
- Images labeled "Image 1" through "Image 26"
- Year: 2025
- Artwork text now displays at bottom (not on hover)
- No dates shown, just image titles

**Home Page:**
- Updated to use `images/home_page.jpg` as background

**Text Display:**
- Removed hover overlay effects
- Text permanently visible below images
- Clean, simple presentation

### Iteration 4 - UI Improvements
**Page Transitions:**
- Added gentle fade effects (0.8s fade-in, 0.6s fade-out)
- Uses cubic-bezier easing for professional feel

**Navigation:**
- Changed "Gallery" to "Works" throughout site

**Home Page:**
- Image changed to 16:9 aspect ratio
- Centered with `object-fit: contain`
- Full viewport height

**Contact:**
- Removed Facebook and LinkedIn
- Only Instagram link with SVG icon (28px)
- Instagram: https://www.instagram.com/michaellamor/

### Iteration 5 - CV Integration
**CV Data Added** (from bio.txt):
- Personal details: Born 1998, Jerusalem
- Email: michaelasga1998@gmail.com
- Phone: 054-3451679
- Education: BFA Bezalel Academy (2019-2023)
- 11 exhibitions (2021-2026)
- Grants and projects
- Collections
- Publications with link

**Page Transitions:**
- Enhanced to 0.8s fade-in
- 0.6s fade-out with smooth cubic-bezier
- Professional, elegant transitions

### Iteration 6 - Refinements
**About Page:**
- Removed artist photo
- Removed large heading
- Single column layout (max-width: 800px)
- Simple text: "Michaela Mor" at top
- User removed personal details, kept "Me: To be continued..."

**Typography:**
- Reduced all body text font sizes
- Artist name: 1.1rem
- Section headings: 0.95rem
- Body text: 0.9rem
- List items: 0.85rem
- Gallery captions: 0.85rem
- More refined, elegant feel

**Font Change:**
- Changed from Julius Sans One (all-caps) to Sofia Sans
- Proper mixed case display

---

## Current File Structure

```
michaela_website/
├── index.html              # Home with 16:9 hero image
├── gallery.html            # Works page with exhibition folders
├── exhibition-1.html       # Bezalel Academy (26 images)
├── exhibition-2.html       # Template
├── exhibition-3.html       # Template
├── exhibition-4.html       # Template
├── about.html              # CV page
├── contact.html            # Email, location, Instagram
├── style.css               # All styles, Sofia Sans font
├── script.js               # Page transitions, lightbox
├── .gitignore              # Excludes "צילומי תערוכות ועבודות"
├── bio.txt                 # CV source data
├── fonts/                  # Julius Sans One, Kumbh Sans, Sofia Sans
├── images/
│   ├── home_page.jpg       # Home page 16:9 image
│   ├── instagram-icon.svg  # Social icon
│   └── Gallery/
│       └── Bezalel Academy/  # 26 artwork images (2-7 MB each)
└── צילומי תערוכות ועבודות/  # Source photos (643 MB - NOT in git)
```

---

## Technical Details

### Fonts
- **Current:** Sofia Sans (mixed case)
- **Available:** Kumbh Sans, Julius Sans One
- **Customization:** Edit CSS variables lines 38-39 in style.css

### Colors
```css
--primary-color: #2c2c2c
--secondary-color: #8b9da8
--text-color: #4a4a4a
--border-color: #f0f0f0
```

### Page Transitions
- Fade-in: 0.8s cubic-bezier(0.4, 0.0, 0.2, 1)
- Fade-out: 0.6s cubic-bezier(0.4, 0.0, 0.2, 1)
- Applied via JavaScript to all internal links

---

## Deployment Status - IN PROGRESS

### Issue Encountered
**Problem:** Cannot push to GitHub Pages due to large image files

**Error:**
```
error: RPC failed; HTTP 400
send-pack: unexpected disconnect while reading sideband packet
Writing objects: 100% (81/81), 88.87 MiB
```

**Root Cause:**
- Repository size: 89 MB
- Individual images: 2-7 MB each (26 images in Bezalel Academy)
- GitHub has strict limits on push size and file sizes

**Git Setup Completed:**
- Repository initialized
- .gitignore configured (excludes source photo folder)
- Initial commit created
- Remote added: https://github.com/MaximIfergan/michaela-mor-portfolio.git
- Push failed due to file sizes

---

## Next Steps (For Next Session)

### Option 1: Compress Images (RECOMMENDED)
**Pros:**
- Scalable - just `git push` for updates
- Better website performance (faster loading)
- Industry best practice
- Works with GitHub Pages

**Process:**
1. Install ImageMagick: `brew install imagemagick`
2. Compress Bezalel images to 85% quality:
   ```bash
   cd "images/Gallery/Bezalel Academy"
   for file in *.jpg; do
     convert "$file" -quality 85 -resize "1920x1920>" -strip "$file"
   done
   ```
3. Commit compressed images
4. Push to GitHub
5. Enable GitHub Pages

**Result:**
- Images reduce from 2-7 MB to ~200-500 KB each
- Faster website, happy visitors
- Git works normally

### Option 2: Use Netlify (ALTERNATIVE)
**Pros:**
- No compression needed
- Handles large files
- Instant deployment

**Process:**
1. Go to netlify.com
2. Drag and drop `michaela_website` folder
3. Get live URL immediately

**Cons:**
- Less scalable (need to re-upload for updates)
- Can connect to Git later if needed

### Option 3: Git LFS (COMPLEX)
Only if you want to keep full-resolution images in Git:
```bash
brew install git-lfs
git lfs install
git lfs track "images/**/*.jpg"
```

---

## Recommended Workflow for Next Session

1. **Compress the images** (Option 1 above)
2. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Compress images for web deployment"
   git push -u origin main
   ```
3. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Source: main branch, / (root)
   - Save
4. **Site live at:** `https://MaximIfergan.github.io/michaela-mor-portfolio/`

5. **For future updates:**
   ```bash
   # Add new exhibition photos (compress first)
   git add images/Gallery/NewExhibition/
   git commit -m "Add New Exhibition"
   git push
   ```

---

## Quick Reference - Key Information

**Repository:** https://github.com/MaximIfergan/michaela-mor-portfolio.git
**Local Path:** /Users/maxim/Programs/Projects/michaela_website
**Artist Email:** michaelasga1998@gmail.com
**Instagram:** @michaellamor

**Navigation:**
- Home → Works → About → Contact
- Works shows exhibition folders
- Each exhibition has its own gallery page
- Lightbox on click for full-size viewing

**To customize fonts:** Edit `style.css` lines 38-39
**To change colors:** Edit `style.css` lines 10-17
**To add exhibitions:** Copy `exhibition-1.html`, update images and title

---

## Summary

Built a complete, professional portfolio website for Michaela Mor. Design is clean, minimal, and elegant. All content is in place. Only remaining task is to compress images and deploy to make the site live on the web.

**Total Cost:** $0 (GitHub Pages is free)
**Domain (optional):** ~$12/year if you want custom domain later

---

*Session ended on deployment preparation. Next session: compress images and deploy.*
