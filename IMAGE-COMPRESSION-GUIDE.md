# Image Compression Guide

## Quick Start

When adding new exhibition photos to your website, always compress them first:

```bash
./compress-images.sh "images/Gallery/Exhibition Name"
```

## Why Compress Images?

- **Fast Loading:** Visitors won't wait for slow images
- **More Storage:** Fit thousands of images instead of hundreds
- **Better SEO:** Google loves fast websites
- **Mobile Friendly:** Saves data for mobile visitors
- **GitHub Compatible:** Required for GitHub Pages deployment

## Current Settings

- **Max Dimension:** 1920px (perfect for web, even 4K displays)
- **Quality:** 85% (industry standard, no visible loss)
- **Result:** Images go from 2-7 MB → 150-300 KB (95% smaller!)

## How to Use

### For New Exhibitions

1. Add your high-res photos to a folder:
   ```
   images/Gallery/My New Exhibition/
   ```

2. Run the compression script:
   ```bash
   ./compress-images.sh "images/Gallery/My New Exhibition"
   ```

3. The script will:
   - Find all .jpg and .png files
   - Resize to 1920px max
   - Compress to 85% quality
   - Remove metadata (EXIF data)
   - Overwrite originals with optimized versions

4. Done! Your images are ready for the web.

### Compress Multiple Folders

```bash
./compress-images.sh "images/Gallery/Exhibition 1"
./compress-images.sh "images/Gallery/Exhibition 2"
./compress-images.sh "images/Gallery/Exhibition 3"
```

## Customizing Settings

Edit `compress-images.sh` to change:

- `MAX_SIZE=1920` → Change max dimension (e.g., 2400 for higher res)
- `QUALITY=85` → Adjust quality (80-90 recommended)
- `STRIP_METADATA=true` → Keep or remove EXIF data

## What Happened to Your Images?

### Before Compression:
- **Resolution:** 3500 × 2333 pixels
- **File Size:** 1.9-4.5 MB each
- **Total (26 images):** 90 MB
- **GitHub:** Can't push (too large)

### After Compression:
- **Resolution:** 1920 × 1280 pixels
- **File Size:** 132-184 KB each
- **Total (26 images):** 7.7 MB
- **GitHub:** ✓ Pushes instantly
- **Visual Quality:** Still stunning!

## Professional Artist Standards

Most professional artist portfolios use:
- 1920-2400px images
- 150-500 KB file sizes
- 80-90% JPEG quality

Your settings match industry best practices.

## Tips

- **Keep Originals:** Store high-res originals separately (they're already in `צילומי תערוכות ועבודות/`)
- **Batch Process:** Compress before adding to git
- **Test First:** Upload one image to check quality before compressing all
- **Web vs Print:** Web needs smaller files; keep originals for prints

## Troubleshooting

**Script won't run:**
```bash
chmod +x compress-images.sh
```

**ImageMagick not found:**
```bash
brew install imagemagick
```

**Need to compress home page image:**
```bash
./compress-images.sh "images"
```
