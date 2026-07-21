# The Dojo Bay — landing page

The clearnet landing page for [The Dojo Bay](https://github.com/Dojobay/dojobay), a public directory of Samourai and Ashigaru Dojo nodes. This repo exists only to introduce the project and help people reach it over Tor. No Dojo data is served here; the directory itself is an onion service and lives in the main repository.

Live at **https://dojobay.org**.

## What's in here

- `index.html` — the entire page (self-contained: inline CSS and a small progressive-enhancement script, no build step, no framework, no third-party requests)
- `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png`, `icon-512.png` — the torii-and-waves mark
- `og-image.png` — 1200×630 social share card
- `CNAME`, `robots.txt`, `sitemap.xml` — hosting and SEO
- `README.md` — this file

## Hosting

Served as a static site from GitHub Pages (Settings → Pages → Deploy from a branch → `main` / root) on the apex domain `dojobay.org`. Keep the publishing source as "Deploy from a branch" rather than a GitHub Actions workflow, since an Actions build ignores the `CNAME` file and would drop the custom domain.

## Making changes

Everything is in `index.html`. The onion address is defined once, in the `data-full` attribute on the address line; the page abbreviates it for display but copies the full URL. If the address ever rotates, change it there. The three brand fonts (Archivo, Hanken Grotesk, JetBrains Mono) fall back to a system stack by default; a commented `@font-face` block explains how to self-host them for an exact match.

## Credits

The Tor onion mark is a trademark of The Tor Project, Inc., used here under CC BY 3.0 US and recoloured. The PayNym logo denotes BIP47 payment-code identity. The Android robot and Apple logo are platform indicators for the download links. All other code and artwork is released under the MIT licence, consistent with the main project.
