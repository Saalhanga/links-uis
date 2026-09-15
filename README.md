# UIS Link-in-Bio Website

A modern, professional link-in-bio page for **United Islamic Society (UIS)**. Built with pure HTML, CSS, and JavaScript. Designed for GitHub Pages hosting.

## Features

- Mobile-first responsive design
- Dark mode with system preference detection and localStorage persistence
- Dynamic link cards generated from a simple JavaScript data file
- Featured link styling
- Social media icon row
- Smooth animations with `prefers-reduced-motion` support
- Accessible (semantic HTML, keyboard navigation, focus states, ARIA labels)
- SEO metadata (Open Graph, Twitter Card, theme-color)

## Project Structure

```
uis-link-page/
├── index.html
├── style.css
├── script.js
├── data/
│   └── links.js
└── assets/
    ├── logo.svg
    ├── favicon.ico
    └── og-image.jpg
```

## Quick Start

1. Clone or download this repository.
2. Open `index.html` in a browser to preview locally.
3. Edit `data/links.js` to update links, titles, descriptions, icons, and featured status.
4. Edit `script.js` to update `UIS_CONFIG` (name, tagline) and `UIS_SOCIALS` (social URLs).
5. Replace `assets/logo.svg`, `assets/favicon.ico`, and `assets/og-image.jpg` with your own assets.

## Deploy to GitHub Pages

1. Push this project to a GitHub repository.
2. Go to **Settings → Pages** in your repository.
3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/root` (or `/docs` if you place files in a `docs` folder)
4. Click **Save**.
5. Your site will be live at: `https://<username>.github.io/<repository-name>/`

## Customization

### Colors
Edit CSS variables in `style.css` under `:root`:

```css
:root {
    --primary: #0f766e;
    --primary-light: #14b8a6;
    --primary-dark: #115e59;
    --secondary: #0d9488;
    --background: #f0fdfa;
    --surface: #ffffff;
    --text: #0f172a;
    --text-secondary: #475569;
    --text-muted: #94a3b8;
    --border: #e2e8f0;
}
```

Dark mode colors are defined under `[data-theme="dark"]` in the same file.

### Links
Edit `data/links.js`. Each link object supports:

- `title` — Display title
- `description` — Short subtitle
- `url` — Target URL
- `icon` — Icon name (see `ICONS` map in `script.js`)
- `featured` — `true` to highlight the card
- `enabled` — `false` to hide the link

### Socials
Update `UIS_SOCIALS` in `script.js`:

```javascript
const UIS_SOCIALS = {
    facebook: "https://facebook.com/yourpage",
    instagram: "https://instagram.com/yourprofile",
    youtube: "https://youtube.com/@yourchannel",
    viber: "https://invite.viber.com/...",
    whatsapp: "https://wa.me/1234567890",
    email: "mailto:contact@example.com"
};
```

### Analytics
Uncomment the placeholder block in `script.js` and insert your analytics code (e.g., Google Analytics).

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

&copy; 2026 United Islamic Society. All rights reserved.

After a minute or two, the site will be live at:
https://saalhanga.github.io/links-uis/
Remaining placeholders to update:
Replace https://example.com URLs in data/links.js with real UIS links
Update social URLs in script.js under UIS_SOCIALS
Replace assets/logo.svg, assets/favicon.ico, and assets/og-image.jpg with actual brand assets
