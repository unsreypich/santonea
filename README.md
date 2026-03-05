# SANTONEA - សន្ទនា

A centralised AI-powered RAG admin dashboard for managing users, conversations, and platform settings.

## Project Structure

```
rag-landing/
├── index.html          # Main HTML file (landing page)
├── styles.css          # External CSS stylesheet
├── README.md           # This file
└── .gitignore          # Git ignore rules
```

## Features

- **Separated HTML & CSS**: Clean separation of concerns for better maintainability
- **Khmer Language Support**: Includes Interfont for optimal Khmer text rendering with Noto Serif Khmer fallback
- **GitHub Pages Ready**: Uses relative paths and minimal dependencies for reliable GitHub Pages deployment
- **Dark/Light Theme**: Toggle between dark and light modes
- **Bilingual Interface**: English and Khmer language support
- **Responsive Design**: Fully responsive across all device sizes

## Local Development

### View locally in browser
Simply open `index.html` in your web browser:
```bash
open index.html
```

Or serve with a local server:
```bash
python3 -m http.server 8000
# Then visit http://localhost:8000
```

## GitHub Pages Deployment

### Step 1: Create a GitHub Repository
```bash
git init
git add .
git commit -m "Initial commit: Landing page for SANTONEA"
git branch -M main
git remote add origin https://github.com/yourusername/rag-landing.git
git push -u origin main
```

### Step 2: Enable GitHub Pages
1. Go to your repository settings
2. Scroll to "GitHub Pages" section
3. Select "main" as the source branch
4. Select "/" (root) as the folder
5. Save

### Step 3: Access Your Site
Your site will be available at: `https://yourusername.github.io/rag-landing/`

## Font Configuration

### Khmer Fonts
The project uses a font stack for Khmer text rendering:
1. **Interfont** (primary - modern Khmer font)
2. **Noto Serif Khmer** (fallback - widely supported)

Both fonts are loaded from CDN, so no local installation is required.

### English Fonts
Uses **Inter** from Google Fonts for a clean, modern look.

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Theme & Language

Both theme and language preferences are stored in `localStorage`:
- Theme preference: `santonea-theme` (light/dark)
- Language preference: `santonea-lang` (en/km)

Preferences persist across browser sessions.

## Customization

### Colors
Edit the CSS variables in `styles.css`:
```css
[data-theme="dark"] {
  --accent: #6c8ef5;
  --gold: #f0c060;
  /* ... more variables ... */
}
```

### Fonts
Update font imports in `index.html` `<head>` section.

### Content
Edit the HTML content in `index.html` while maintaining the class structure for styles to apply correctly.

## Troubleshooting

### Khmer text not displaying correctly
- Clear browser cache (Cmd+Shift+R on Mac)
- Ensure fonts are loading from CDN (check Network tab in DevTools)
- Fallback to Noto Serif Khmer should work if Interfont CDN is unavailable

### Styles not loading on GitHub Pages
- Verify that `styles.css` is in the same directory as `index.html`
- Check browser console for any 404 errors
- Ensure relative paths are used (no leading `/`)

### JavaScript not working
- Check browser console for errors
- Ensure JavaScript is enabled
- Verify that the script tag is in the HTML body

## Performance

- **CSS**: Minified and optimized at 20KB
- **Fonts**: Loaded from Google Fonts and Apple CDN (cached globally)
- **JavaScript**: Minimal inline script (~2KB), no external dependencies
- **Images**: SVG icons for crisp rendering

## License

© 2026 SANTONEA. Built for internal administration.

## Support

For issues or questions, please create an issue in the repository.
