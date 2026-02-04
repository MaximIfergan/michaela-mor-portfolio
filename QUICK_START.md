# Quick Start Guide

## 1️⃣ Add Your Images (5 minutes)

Put these images in the `images/` folder:

**Required:**
- `hero-bg.jpg` - Hero background (use any striking artwork)
- `artist-photo.jpg` - Photo of your girlfriend
- `featured-1.jpg`, `featured-2.jpg`, `featured-3.jpg` - Three featured artworks
- `artwork-1.jpg` through `artwork-6.jpg` - Six gallery images (add more if you want)

**Quick tip:** You can temporarily use the same image multiple times just to see how it looks, then replace them later.

## 2️⃣ Test It Locally (1 minute)

1. Open `index.html` in your web browser
2. Click around to see all pages
3. Try the gallery lightbox (click on images)

## 3️⃣ Customize Content (15 minutes)

### Update Artist Name
Search and replace "Artist Name" in all HTML files with your girlfriend's name.

### Edit About Page
Open `about.html` and fill in:
- Artist bio (the paragraph sections)
- Education
- Exhibitions
- Awards

### Edit Contact Page
Open `contact.html` and update:
- Email address
- Phone number
- Location
- Social media links

### Edit Gallery
In `gallery.html`, update each artwork's:
- `data-title` - Artwork name
- `data-year` - Year created
- `data-medium` - Medium (Oil on canvas, Acrylic, etc.)
- Image filename

## 4️⃣ Deploy It (10 minutes)

### Easiest Method: Netlify Drop

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag your entire `michaela_website` folder
3. Get instant live URL
4. Done!

### Best Method: GitHub Pages

```bash
# In your project folder, run:
git init
git add .
git commit -m "Initial commit"

# Create a new repo on github.com, then:
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
git push -u origin main

# Enable GitHub Pages in repo settings
```

## 5️⃣ Optional: Add Custom Domain

1. Buy domain from Namecheap/Porkbun (~$10/year)
2. Point it to your Netlify/GitHub Pages
3. Follow their DNS setup guides

---

## Quick Customization Examples

### Change Colors
Edit `style.css` lines 10-16:
```css
--secondary-color: #5b8db0;  /* Change this to any color */
```

### Add More Gallery Items
Copy-paste this in `gallery.html`:
```html
<div class="gallery-item" data-title="Sunset" data-year="2024" data-medium="Oil on canvas">
    <img src="images/sunset.jpg" alt="Sunset">
    <div class="gallery-item-info">
        <h3>Sunset</h3>
        <p>2024</p>
    </div>
</div>
```

### Make Contact Form Work
Replace form in `contact.html` with:
```html
<form action="https://formspree.io/f/YOUR_ID" method="POST">
```
(Get free ID from formspree.io)

---

## Need Help?

1. Check `README.md` for detailed instructions
2. Google error messages
3. Ask ChatGPT/Claude for help with specific issues

You've got this! 🎨
