# IN10C5 Official Website

Marketing website for **IN10C5 India Private Limited**: the AI trust layer for modern commerce.
A static site (plain HTML, CSS and JavaScript) with no build step.

Live site: https://in10c5-india.github.io/IN10C5-Official-Website/

## Project structure

```
.
├── index.html              Home page (all sections, styles and scripts are inline)
├── privacy-policy.html     Privacy policy
├── terms.html              Terms of use
├── assets/
│   ├── css/
│   │   └── legal.css       Styles shared by the privacy and terms pages
│   └── images/
│       ├── favicon/        Favicon (favicon-96.png is the one the site uses)
│       ├── logo/           Logo files (logo-nav.png is used on the legal pages)
│       ├── icons/          Source artwork for the hero diagram icons
│       └── integrations/   Source logos for the integrations section
├── .gitignore
└── README.md
```

`index.html` embeds its own images as inline data so the home page loads as a single file.
The files in `assets/images/icons` and `assets/images/integrations` are the source artwork for those
embedded images, kept so they can be edited and re-exported.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

The site is published with GitHub Pages from the `main` branch. Push to `main` and it updates in a minute or two.

```bash
git add .
git commit -m "Describe your change"
git pull --rebase origin main
git push origin main
```

## Notes

- All page links are relative (for example `privacy-policy.html`), so the site works under the `/IN10C5-Official-Website/` address on GitHub Pages.
- The contact form opens the visitor's email app addressed to help@in10c5.com. There is no server.
