# HTML Tools Registry

Single-file HTML tools collection with bilingual support.

## Quick Start

### Local Development

1. Clone the repository
2. Open `index.html` in a browser (requires a local server)

```bash
# Using Python
python -m http.server 8080

# Using Node.js
npx serve .
```

### Deploy to GitHub Pages

1. Go to Settings → Pages
2. Source: Deploy from main branch
3. The site will be available at `https://{username}.github.io/{repo}`

## Features

- Tool listing with cards
- Live iframe preview
- Bilingual support (English/Chinese)
- Add tool form with patch generator
- GitHub Actions validation

## Project Structure

```
html-tools-registry/
├── index.html          # Main page
├── tools.json          # Tool manifest
├── CONTRIBUTING.md    # Contribution guide
├── tools/             # Tool files
│   ├── sql-monthly-splitter/
│   └── sql-replacer/
├── i18n/              # Language files
│   ├── en.json
│   └── zh.json
└── .github/
    ├── workflows/
    │   └── validate.yml
    └── PULL_REQUEST_TEMPLATE.md
```

## License

MIT