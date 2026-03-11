# SnapTools — Free Online Image Tools

**SnapTools** is a free, privacy-first collection of browser-based image editing tools. All image processing happens entirely in your browser using the HTML5 Canvas API — your images never leave your device.

🌐 **Live site:** [snaptools.app](https://snaptools.app)

## Features

- 🗜️ **Image Compressor** — Reduce file sizes up to 90% while preserving quality. Supports JPEG, PNG, and WebP.
- 🔄 **Format Converter** — Convert between PNG, JPEG, WebP, and BMP formats instantly.
- 📐 **Image Resizer** — Resize images to exact dimensions or scale by percentage.
- ✂️ **Smart Crop** — Crop images to popular aspect ratios (1:1, 4:3, 16:9) or custom dimensions.
- 💧 **Watermark Maker** — Add customizable text watermarks with adjustable font, size, and opacity.
- 🎨 **Photo Filters** — Apply professional filters including grayscale, sepia, blur, brightness, and contrast.

## Privacy First

SnapTools is built on a simple principle: **your images stay on your device**. There are no uploads, no server-side processing, and no data collection. All tools run entirely in the browser using client-side JavaScript and the HTML5 Canvas API.

## Technology

- Pure HTML5, CSS3, and vanilla JavaScript
- HTML5 Canvas API for image processing
- No external dependencies or frameworks
- Responsive design for desktop and mobile
- Dark theme with modern UI

## Getting Started

Since SnapTools is a static website, no build process is required. Simply open `index.html` in your browser or serve the files with any static web server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .
```

Then visit `http://localhost:8000` in your browser.

## Project Structure

```
├── index.html                 # Home page with tool cards
├── image-compressor.html      # Image compression tool
├── format-converter.html      # Format conversion tool
├── image-resizer.html         # Image resizing tool
├── smart-crop.html            # Smart cropping tool
├── watermark-maker.html       # Watermark creation tool
├── photo-filters.html         # Photo filter tool
├── faq.html                   # Frequently asked questions
├── about.html                 # About page
├── contact.html               # Contact form
├── privacy-policy.html        # Privacy policy
├── terms-of-service.html      # Terms of service
├── blog/                      # Blog articles
│   ├── index.html
│   └── *.html
├── css/
│   └── style.css              # Global stylesheet
├── robots.txt                 # Search engine directives
├── sitemap.xml                # XML sitemap for SEO
└── ads.txt                    # AdSense publisher verification
```

## License

MIT License — see [LICENSE](LICENSE) for details.

© 2026 Ying Wang
