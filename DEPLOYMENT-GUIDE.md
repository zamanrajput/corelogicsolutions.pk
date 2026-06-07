# CoreLogic Solutions — SEO Deployment Checklist

## Files in this package

| File | Deploy to | Purpose |
|------|-----------|---------|
| `sitemap.xml` | https://corelogicsolutions.pk/sitemap.xml | Tells Google all your URLs |
| `robots.txt` | https://corelogicsolutions.pk/robots.txt | Controls crawler access |
| `site.webmanifest` | https://corelogicsolutions.pk/site.webmanifest | PWA + browser metadata |
| `meta-tags.html` | Paste into `<head>` of `index.html` | Full SEO + OG + Twitter meta |
| `schema-structured-data.html` | Paste into `<head>` of `index.html` | Rich snippets (FAQ, LocalBusiness, etc.) |

---

## Step-by-step deployment

### 1. Upload files to server root
- `sitemap.xml` → `/public_html/sitemap.xml`
- `robots.txt` → `/public_html/robots.txt`
- `site.webmanifest` → `/public_html/site.webmanifest`

### 2. Update index.html
- **Replace** the existing `<meta>` tags in `<head>` with everything from `meta-tags.html`
- **Add** all `<script type="application/ld+json">` blocks from `schema-structured-data.html` just before `</head>`

### 3. Create OG image
- Create `og-image.png` (1200×630px) with your logo + tagline
- Upload to `/public_html/og-image.png`

### 4. Create favicon set
Generate from your logo at https://realfavicongenerator.net — upload the result to server root:
- `favicon.ico`
- `favicon-16x16.png`
- `favicon-32x32.png`
- `apple-touch-icon.png`
- `android-chrome-192x192.png`
- `android-chrome-512x512.png`

### 5. Google Search Console
1. Go to https://search.google.com/search-console
2. Add property → `https://corelogicsolutions.pk`
3. Verify via HTML tag method (paste the `<meta name="google-site-verification" .../>` into your `<head>`)
4. After verified → Sitemaps → submit `https://corelogicsolutions.pk/sitemap.xml`

### 6. Bing Webmaster Tools (bonus — gets you Bing + DuckDuckGo)
1. Go to https://www.bing.com/webmasters
2. Add site and verify
3. Import from Google Search Console (one-click option available)

### 7. Test everything
- **Rich results test**: https://search.google.com/test/rich-results
- **OG preview**: https://www.opengraph.xyz
- **robots.txt test**: Google Search Console → Settings → robots.txt tester
- **Mobile friendly**: https://search.google.com/test/mobile-friendly
- **Page speed**: https://pagespeed.web.dev

---

## Quick wins after indexing
- Add Google Business Profile listing (free) for Lahore local SEO
- Post the FBR E-Invoice product on LinkedIn and Facebook with the site link to generate backlinks
- Get listed on pakistansoftwarehouses.com and similar directories
