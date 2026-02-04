# Updated Website Structure

## Changes Made

### 1. Removed Elements
- ✅ Featured Work section from home page
- ✅ Contact form ("Send a Message")
- ✅ Copyright footer banner

### 2. Gallery Now Shows Exhibitions
The gallery page now displays **exhibition folders** instead of individual artworks. Each exhibition has:
- A cover photo
- Title
- Year
- Link to its own detailed gallery page

### 3. Simplified Contact Page
Now shows just:
- Email
- Phone
- Location
- Social media links

### 4. Gentler Styling
- Softer border colors (#f0f0f0 instead of #e0e0e0)
- More muted accent color (#8b9da8 instead of #5b8db0)
- Subtle hover effects (opacity changes instead of color shifts)
- Transparent footer with minimal border
- Cleaner, less prominent headers

## File Structure

```
michaela_website/
├── index.html              # Home page (hero only)
├── gallery.html            # Exhibition folders
├── exhibition-1.html       # Individual exhibition galleries
├── exhibition-2.html
├── exhibition-3.html
├── exhibition-4.html
├── about.html
├── contact.html
├── style.css
├── script.js
└── images/
    ├── hero-bg.jpg
    ├── artist-photo.jpg
    ├── exhibition-1-cover.jpg    # Cover images for exhibitions
    ├── exhibition-2-cover.jpg
    ├── exhibition-3-cover.jpg
    ├── exhibition-4-cover.jpg
    ├── ex1-artwork-1.jpg         # Individual artworks per exhibition
    ├── ex1-artwork-2.jpg
    ├── ex2-artwork-1.jpg
    └── ...
```

## How to Add Images

### For Gallery Page (Exhibition Covers)
1. Create cover images for each exhibition:
   - `exhibition-1-cover.jpg`
   - `exhibition-2-cover.jpg`
   - etc.

### For Individual Exhibition Pages
Name images by exhibition:
- Exhibition 1: `ex1-artwork-1.jpg`, `ex1-artwork-2.jpg`, etc.
- Exhibition 2: `ex2-artwork-1.jpg`, `ex2-artwork-2.jpg`, etc.

## How to Add New Exhibitions

1. **Copy an existing exhibition file:**
   ```bash
   cp exhibition-1.html exhibition-5.html
   ```

2. **Edit the new file:**
   - Update the title
   - Change the exhibition name and year
   - Update image filenames (ex5-artwork-1.jpg, etc.)

3. **Add to gallery.html:**
   ```html
   <a href="exhibition-5.html" class="exhibition-folder">
       <img src="images/exhibition-5-cover.jpg" alt="Exhibition 5">
       <div class="exhibition-info">
           <h3>Your Exhibition Title</h3>
           <p>2025</p>
       </div>
   </a>
   ```

4. **Add images to the images folder:**
   - `exhibition-5-cover.jpg`
   - `ex5-artwork-1.jpg`, `ex5-artwork-2.jpg`, etc.

## Quick Customization

### Change Artist Name
Find and replace "Artist Name" in all HTML files.

### Update Colors
Edit `style.css` (lines 10-17):
```css
:root {
    --secondary-color: #8b9da8;  /* Change for different accent */
    --text-color: #4a4a4a;       /* Main text color */
    --border-color: #f0f0f0;     /* Border color */
}
```

### Update Contact Info
Edit `contact.html` with real email, phone, location, and social links.

## Testing

Open `index.html` in your browser to see the site. Click through:
- Home → Gallery → Individual Exhibition
- About page
- Contact page

All navigation and lightbox functionality should work without a server.
