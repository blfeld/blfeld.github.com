# blfeld.github.io — Personal Academic Website

Personal website of Bennet Feld, Ph.D. Candidate in Economics at LSE.
Live at: **https://blfeld.github.io**

Built on the [Minimal Light](https://github.com/yaoyao-liu/minimal-light) Jekyll theme, hosted on GitHub Pages.

---

## Running locally

You need Ruby 3+ (installed via Homebrew) and Bundler.

### First-time setup

```bash
# 1. Install Homebrew if you don't have it
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# 2. Install Ruby
brew install ruby

# 3. Add Ruby to your PATH (do this once, then restart terminal)
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

# 4. Install Bundler and gems
cd ~/Library/CloudStorage/Dropbox/Projects/Website
gem install bundler
bundle install
```

### Start the server

```bash
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
cd ~/Library/CloudStorage/Dropbox/Projects/Website
bundle exec jekyll serve --livereload
```

Then open **http://127.0.0.1:4000** in your browser. The site auto-refreshes when you save a file.

### Deploy

Just push to `main` on GitHub — GitHub Pages rebuilds automatically within ~1 minute.

```bash
git add .
git commit -m "your message"
git push
```

---

## Editing content

All content lives in two files:

### `index.md`
The homepage text — About Me, Research Interests, Work in Progress. Edit this directly in Markdown.

### `_data/publications.yml`
Add publications here. Each entry supports:

```yaml
- title: "Paper title"
  authors: "Author One, Author Two, and Author Three"   # HTML links are supported
  abstract: "Abstract text..."
  pdf: "https://link-to-pdf.com"
  notes: "Working Paper"   # shown as a label
```

### `_config.yml`
Site-wide settings: your name, position, affiliation, email, social links, Google Analytics ID.

---

## Design

### Colors

| Element | Light mode | Dark mode |
|---------|-----------|-----------|
| Page background | `#FFFDF1` (warm cream) | `#576A8F` (steel blue) |
| Sidebar panel | `#FFCE99` (peach) | `#B7BDF7` (lavender) |
| Headings | `#562F00` (dark brown) | `#FFF8DE` (warm cream) |
| Links | `#FF9644` (orange) | `#FF7444` (warm red-orange) |

### Font
**Inter** — loaded from Google Fonts. Closest free equivalent to Graphik (a commercial font by Commercial Type). To switch to Graphik if you have a license, replace the `@import` line in `assets/css/font_sans_serif.css` with your Adobe Fonts embed code and update the font-family.

### Favicon
Uses the official LSE 32×32 favicon fetched from lse.ac.uk.

### Customising styles
All styles are in `_sass/minimal-light.scss`. The no-dark-mode variant is in `_sass/minimal-light-no-dark-mode.scss`.

---

## File structure

```
├── _config.yml              # site settings (name, links, analytics)
├── index.md                 # homepage content
├── _data/
│   └── publications.yml     # publication entries
├── _includes/
│   ├── publications.md      # publications display template
│   └── services.md          # (unused — placeholder from theme)
├── _layouts/
│   └── homepage.html        # main HTML layout
├── _sass/
│   ├── minimal-light.scss               # all styles (dark mode aware)
│   └── minimal-light-no-dark-mode.scss  # styles for no-dark-mode variant
├── assets/
│   ├── css/                 # compiled CSS + font imports
│   ├── img/                 # profile photo, favicon
│   ├── files/               # curriculum_vitae.pdf
│   └── js/                  # favicon switcher, mobile scale fix
└── hidden/
    └── interviewer.md       # unlisted page (accessible by URL only)
```

---

## Google Search

- Google Search Console is set up (verification file: `google222eeae71b43e8d7.html`)
- A sitemap is auto-generated at `https://blfeld.github.io/sitemap.xml` via `jekyll-sitemap`
- To submit the sitemap: go to [Google Search Console](https://search.google.com/search-console) → Sitemaps → enter `sitemap.xml`
