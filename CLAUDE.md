# CLAUDE.md — SnapTools

## Project Overview

SnapTools is a free, privacy-first collection of browser-based image editing tools. All image processing happens entirely in the browser using the HTML5 Canvas API — images never leave the user's device. Live at https://snaptools.app.

## Tech Stack

- **HTML5** — All pages and tool interfaces
- **CSS3** — Single global stylesheet (`css/style.css`) with CSS variables, flexbox, grid
- **Vanilla JavaScript** — Embedded in `<script>` tags within each HTML file; no frameworks or libraries
- **No build system** — Static site, no bundler, no package manager, no dependencies

## Repository Structure

```
/
├── index.html                 # Landing page with tool cards
├── image-compressor.html      # Tool: image compression
├── format-converter.html      # Tool: format conversion
├── image-resizer.html         # Tool: image resizing
├── smart-crop.html            # Tool: smart cropping
├── watermark-maker.html       # Tool: watermark creation
├── photo-filters.html         # Tool: photo filters
├── about.html                 # About page
├── contact.html               # Contact form
├── faq.html                   # FAQ page
├── privacy-policy.html        # Privacy policy
├── terms-of-service.html      # Terms of service
├── blog/                      # Blog section
│   ├── index.html
│   └── *.html                 # Educational blog posts
├── css/
│   └── style.css              # Global stylesheet (~526 lines)
├── robots.txt                 # SEO: search engine directives
├── sitemap.xml                # SEO: XML sitemap
├── ads.txt                    # Google AdSense publisher verification
├── LICENSE                    # MIT License
└── README.md
```

## Running Locally

No build step needed. Serve with any static file server:

```sh
python -m http.server 8000
# or
npx serve .
```

Then open http://localhost:8000.

## Code Conventions

### HTML Pages
- Each tool page is a self-contained HTML file with embedded `<script>` tags
- All pages share a common header/footer structure (copy-pasted, not templated)
- Every page includes: Google Fonts CDN link, `css/style.css`, Open Graph meta tags, and Google AdSense script
- Structured data (JSON-LD) is included on key pages for SEO

### JavaScript Patterns
- State managed via a simple object: `const state = {}`
- Common utility functions per tool: `loadImage()`, `formatBytes()`, `downloadCanvas()`, `setupDropZone()`
- File handling uses `File` API, `FileReader`, `URL.createObjectURL()`
- Canvas operations via `canvas.getContext('2d')`, `drawImage()`, `toBlob()`
- `setupDropZone()` called at page load for drag-and-drop initialization
- Event listeners attached with `addEventListener()`

### CSS (`css/style.css`)
- Dark theme using CSS custom properties (`--bg`, `--surface`, `--text`, `--accent`, etc.)
- Responsive design with mobile-first media queries
- Component classes: `.tool-card`, `.workspace`, `.controls`, `.preview-area`
- Accent color: purple (`#6c5ce7`)

### SEO & Monetization
- Google AdSense client ID: `ca-pub-5454343993694013`
- Open Graph tags on all pages
- `sitemap.xml` must be updated when adding new pages
- `robots.txt` allows all crawlers

## Important Notes

- **No tests or linting configured** — verify changes by opening pages in a browser
- **No templating** — header/footer changes must be applied to all 18 HTML files manually
- **Privacy-first** — all image processing must stay client-side; never send images to a server
- **Zero dependencies** — do not introduce npm packages or external JS libraries
