# Deployment Instructions

## What's Included

This minimal project contains only the essential files for your Torah visualization:

- `index.html` - The main Torah scroll visualization page
- `assets/fonts/ShlomosemiStam.ttf` - Hebrew font file
- `src/data/pages/torah/*.json` - All 245 Torah text data files
- `.github/workflows/deploy.yml` - Automatic GitHub Pages deployment
- `README.md` - Project documentation
- `.gitignore` - Git ignore rules

## Deploy to GitHub Pages

1. Create a new repository on GitHub (e.g., `torah-visualization`)

2. Add the GitHub remote and push:
   ```bash
   git remote add origin https://github.com/yourusername/torah-visualization.git
   git branch -M main
   git push -u origin main
   ```

3. Enable GitHub Pages:
   - Go to your repository settings
   - Navigate to "Pages" in the left sidebar
   - Under "Source", select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"

4. Your site will be available at: `https://yourusername.github.io/torah-visualization`

## Local Testing

To test locally before deploying:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000 in your browser.

## File Structure

```
torah-visualization-static/
├── index.html                 # Main page (renamed from torah-zoom.html)
├── assets/
│   └── fonts/
│       └── ShlomosemiStam.ttf # Hebrew font
├── src/
│   └── data/
│       └── pages/
│           └── torah/         # 245 JSON files (1.json - 245.json)
├── .github/
│   └── workflows/
│       └── deploy.yml         # Auto-deployment
├── README.md
├── .gitignore
└── DEPLOYMENT.md             # This file
```

Total size: ~6MB (mostly the Torah JSON data files)
