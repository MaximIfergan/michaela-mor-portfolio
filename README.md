# Artist Portfolio Website

A clean, minimal portfolio website for showcasing artwork. Built with pure HTML, CSS, and JavaScript.

## 📁 Project Structure

```
michaela_website/
├── index.html          # Home page with featured work
├── gallery.html        # Full gallery with lightbox
├── about.html          # About the artist
├── contact.html        # Contact information and form
├── style.css           # All styles
├── script.js           # Interactive functionality
├── images/             # Store artwork images here (create this folder)
│   ├── hero-bg.jpg
│   ├── artist-photo.jpg
│   ├── featured-1.jpg
│   ├── artwork-1.jpg
│   └── ...
└── README.md          # This file
```

## 🚀 Getting Started

### 1. Add Images

Create an `images` folder and add your artwork photos:

```bash
mkdir images
```

You'll need:
- `hero-bg.jpg` - Background image for the home page hero section
- `artist-photo.jpg` - Photo of the artist for the About page
- `featured-1.jpg`, `featured-2.jpg`, `featured-3.jpg` - Featured artwork for home page
- `artwork-1.jpg`, `artwork-2.jpg`, etc. - Gallery images

**Tip:** Name your images descriptively (e.g., `sunset-painting-2024.jpg`) for easier management.

### 2. Customize Content

Open each HTML file and replace placeholder text:

- **index.html**: Update artist name, titles, and featured work
- **gallery.html**: Add more gallery items, update artwork titles, years, and mediums
- **about.html**: Add artist bio, education, exhibitions, awards
- **contact.html**: Update email, phone, location, social media links

### 3. Test Locally

Open `index.html` in your web browser to see the site locally.

## 🎨 Customization

### Colors

Edit the CSS variables in `style.css` (lines 10-16):

```css
:root {
    --primary-color: #2c2c2c;      /* Main dark color */
    --secondary-color: #5b8db0;    /* Accent color (links, buttons) */
    --text-color: #333;            /* Body text */
    --light-gray: #f5f5f5;         /* Background sections */
    --white: #ffffff;              /* White */
}
```

### Fonts

The site uses Georgia (serif) by default. To change fonts:

1. Visit [Google Fonts](https://fonts.google.com/)
2. Choose a font and copy the `<link>` tag
3. Add it to the `<head>` of each HTML file
4. Update `font-family` in `style.css`

Example:
```css
body {
    font-family: 'Playfair Display', serif;
}
```

### Adding More Gallery Items

In `gallery.html`, duplicate this block and update the details:

```html
<div class="gallery-item" data-title="New Artwork" data-year="2024" data-medium="Oil on canvas">
    <img src="images/new-artwork.jpg" alt="New Artwork">
    <div class="gallery-item-info">
        <h3>New Artwork</h3>
        <p>2024</p>
    </div>
</div>
```

## 📮 Making the Contact Form Work

The contact form currently shows a success message but doesn't send emails. To make it functional, use one of these **free** options:

### Option 1: Formspree (Easiest)
1. Go to [formspree.io](https://formspree.io/)
2. Sign up for free (50 submissions/month)
3. Create a form and get your form endpoint
4. Update the form in `contact.html`:
```html
<form id="contactForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Option 2: Netlify Forms
If you deploy to Netlify (see below), add `netlify` attribute to the form:
```html
<form id="contactForm" netlify>
```

### Option 3: EmailJS
1. Sign up at [emailjs.com](https://www.emailjs.com/) (200 emails/month free)
2. Follow their JavaScript integration guide
3. Update `script.js` with their code

## 🌐 Deploying Your Website

### Option 1: GitHub Pages (Recommended - Free & Easy)

1. **Create a GitHub account** at [github.com](https://github.com)

2. **Install Git** (if not already installed):
   - Mac: `brew install git` or download from [git-scm.com](https://git-scm.com/)
   - Already have it on most systems

3. **Initialize Git in your project**:
```bash
cd /Users/maxim/Programs/Projects/michaela_website
git init
git add .
git commit -m "Initial commit: Artist portfolio website"
```

4. **Create a new repository on GitHub**:
   - Go to github.com and click "New repository"
   - Name it (e.g., `artist-portfolio`)
   - Don't initialize with README (you already have files)
   - Click "Create repository"

5. **Push your code**:
```bash
git remote add origin https://github.com/YOUR_USERNAME/artist-portfolio.git
git branch -M main
git push -u origin main
```

6. **Enable GitHub Pages**:
   - Go to repository Settings → Pages
   - Source: Deploy from branch `main`
   - Folder: `/ (root)`
   - Click Save

Your site will be live at: `https://YOUR_USERNAME.github.io/artist-portfolio/`

### Option 2: Netlify (Also Free, Drag & Drop)

1. Go to [netlify.com](https://www.netlify.com/) and sign up
2. Drag your project folder into Netlify
3. Your site is live instantly with a free subdomain
4. Optional: Add a custom domain

### Option 3: Vercel (Free, Similar to Netlify)

1. Go to [vercel.com](https://vercel.com/) and sign up
2. Import your GitHub repository (or upload directly)
3. Deploy with one click

## 💰 Costs Breakdown

- **Hosting**: $0 (GitHub Pages/Netlify/Vercel)
- **Domain** (optional): $10-15/year
  - Buy from [Namecheap](https://www.namecheap.com/), [Google Domains](https://domains.google/), or [Porkbun](https://porkbun.com/)
  - Connect to GitHub Pages/Netlify following their guides
- **Total**: $0-15/year

## 🛠 Next Steps & Improvements

Once you're comfortable with the basics, consider:

1. **Add a blog/news section** for exhibitions and updates
2. **Optimize images** - Use [TinyPNG](https://tinypng.com/) to compress images
3. **Add SEO** - Meta descriptions, Open Graph tags
4. **Google Analytics** - Track visitors
5. **Add a favicon** - Small icon in browser tab
6. **Progressive enhancement** - Add subtle animations, loading states

## 📚 Learning Resources

- **HTML/CSS Basics**: [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn)
- **JavaScript**: [javascript.info](https://javascript.info/)
- **Git**: [Git Handbook](https://guides.github.com/introduction/git-handbook/)
- **Web Design**: [Awwwards](https://www.awwwards.com/) for inspiration

## 🆘 Troubleshooting

**Images not showing?**
- Check that image paths are correct
- Make sure images are in the `images/` folder
- Check file extensions match (`.jpg` vs `.jpeg`)

**Gallery lightbox not working?**
- Open browser console (F12) to check for JavaScript errors
- Make sure `script.js` is loading correctly

**Styles not applying?**
- Clear browser cache (Ctrl/Cmd + Shift + R)
- Check that `style.css` link is correct in HTML

## 📝 License

This is a template for personal use. Customize it as you wish!

---

**Need help?** Feel free to ask me any questions as you build and customize the site.
