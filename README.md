# MB Hospitality & Management — static website

## Deploy to GitHub + Cloudflare Pages
1. Extract the ZIP and upload **the contents of this folder** to the root of your GitHub repository.
2. In Cloudflare Pages choose the repository.
3. Framework preset: **None**.
4. Build command: leave empty.
5. Build output directory: `/` (repository root).
6. Deploy. Cloudflare will read `_headers` and `_redirects` automatically.

## Required before production / indexing
- Replace `https://mb-hospitality.pages.dev` everywhere with the final domain.
- Fill every `{{PLACEHOLDER}}` listed in `PLACEHOLDERS.md`.
- Have the Austrian Impressum and privacy wording checked against the final legal/company status and contracts.
- Replace the placeholder `assets/img/logo.svg` with the final logo while preserving the filename.

## Font note
The stylesheet is designed for **Marcellus / Inter Tight / Archivo**, but this ZIP does not redistribute font binaries. Until licensed self-hosted WOFF2 files are added, system fallbacks are used. If you add licensed files yourself, place them in `assets/fonts/` and restore matching `@font-face` declarations plus a single display-font preload.

## Contact form
The form posts directly to Web3Forms using the access key from the brief and redirects to localized thank-you routes. Test all three forms after production deployment and verify the receiving mailbox before launch.

## Click-to-load map
No map request is made on initial page load. The visitor must click the map button first, after which an OpenStreetMap iframe is inserted. CSP therefore includes `frame-src https://www.openstreetmap.org` as the minimum technical exception required for this requested feature.

## Add a case study
Open the localized references page, duplicate the `.case-shell` block, replace the project placeholders only with approved information, then add equivalent localized content to DE, EN and HR pages.

## Add a language
Duplicate the full route tree, add the new route mapping to `assets/js/app.js`, add reciprocal `hreflang` tags, then include the new URLs in `sitemap.xml`.

## Route-count note
The brief says “17 pages × 3” and separately lists routes that total **19 core pages per language** (home + about + approach + services hub + six service pages + industries hub + three industry pages + process + references + contact + imprint + privacy). This build follows the explicit route list, so the sitemap contains **57 core URLs** plus separate noindex thank-you pages.

## Performance notes
- No framework, jQuery, GSAP, page builder or smooth-scroll library.
- One deferred JS file.
- Hero is text-led; no hero photo is required for LCP.
- Media slots reserve dimensions.
- Reduced-motion mode shows final content immediately.
- All tracking is absent by default. If Cloudflare Web Analytics is later enabled, review the final privacy wording.
