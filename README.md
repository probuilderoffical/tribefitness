# Tribe Fitness website

A lightweight, mobile-first static website for Tribe Fitness, Pakistan. The primary conversion path is WhatsApp at **+923202051662**.

## Stack

Semantic HTML, modular CSS and vanilla JavaScript. There is no framework, build dependency or runtime package requirement. This keeps the project fast, GitHub Pages friendly and straightforward to convert to WordPress later.

## Local setup

Clone this authorized repository and serve the repository root with any static server. For example, use a local editor's static preview. Because all asset links are relative, the site also works from the GitHub Pages project subpath.

## Content editing

- `assets/js/content.js`: training programs, FAQs and gallery entries.
- `index.html`: core page copy, contact details and section structure.
- `assets/css/styles.css`: design tokens and responsive presentation.
- Gallery entries are intentionally placeholders. Replace them only with authentic approved Tribe Fitness images; when real image files are added, update the gallery renderer in `main.js` to output responsive `<img>` elements with meaningful alt text, width/height, `loading="lazy"` and `decoding="async"`.
- Address, map, timings, pricing, social profiles, trainer names and testimonials are intentionally omitted/pending verification. Do not publish guesses.
- The testimonials container is hidden in `index.html` and should only be activated with authentic approved quotes.

## WhatsApp conversion

The public number is stored without punctuation as `923202051662` in `content.js`, while visible copy uses **+923202051662**. CTAs use `wa.me`. The contact form does not submit to a server; it builds a pre-filled WhatsApp message and hands the visitor off to WhatsApp.

## SEO and accessibility

The homepage includes title/description metadata, Open Graph metadata, canonical URL and schema.org `HealthClub` structured data. `robots.txt` and `sitemap.xml` are included. The UI includes semantic landmarks, a skip link, visible focus states, accessible navigation state, labelled form controls, keyboard-operable FAQ and native-dialog lightbox, and reduced-motion handling.

When a verified street address is available, add it to visible contact content and expand the schema `PostalAddress`. Add a map only after the address is verified.

## GitHub Pages deployment

`.github/workflows/pages.yml` deploys the repository root as a static Pages artifact on pushes to `main` and supports manual runs. Repository Pages must be configured to use **GitHub Actions** as the source. The expected project URL is:

`https://probuilderoffical.github.io/tribefitness/`

The URL is only live after Pages is enabled and a successful deployment completes.

## WordPress conversion checklist

See `WORDPRESS-MAPPING.md` for section-by-section mapping. In summary:

- Move global design tokens from `:root` into theme CSS/custom properties.
- Convert header/footer into `header.php` / `footer.php` or template parts.
- Convert each homepage `<section>` into a simple template part or Gutenberg block pattern.
- Move `TRIBE_CONTENT` arrays to WordPress fields, block attributes or an options page.
- Preserve WhatsApp URL building and verified-content rules.
- Register and enqueue CSS/JS rather than inlining assets.
- Replace gallery placeholders with Media Library images and responsive WordPress image functions.
- Populate schema/address/social data only from verified business information.
- Re-test keyboard navigation, responsive layouts, metadata and structured data after conversion.

## Content integrity

No pricing, physical address, opening hours, member counts, awards, trainer identities, performance results or testimonials are claimed because these facts were not supplied as verified information.
