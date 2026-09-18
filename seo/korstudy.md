# KORstudy — UX Writing, Content Strategy & Technical SEO

**Site:** [easy-korean-learning.netlify.app](https://easy-korean-learning.netlify.app/)  
**Role:** Founder · UX Writer · Content Designer · Frontend Developer · SEO Specialist (end-to-end)  
**Timeline:** 2025–2026  
**Tools:** Screaming Frog SEO Spider · Google Search Console · Google Analytics 4 · Rich Results Test · PageSpeed Insights

---

## Overview

**KORstudy** is a Ukrainian-language web platform for learning Korean: courses TOPIC 1–6, free lessons, a Hangul reference, blog, news, and student reviews.

Most Korean-learning resources online are in English or Russian. Ukrainian speakers — students, future exchange participants, K-pop and K-drama fans — had almost no native-language platform to learn from. KORstudy was built to fill that gap.

I designed, built, and wrote the entire platform end-to-end: UX copy, information architecture, frontend development, technical SEO, and privacy compliance.

---

## Context

- **Problem:** Ukrainian-speaking learners had no structured, native-language platform for Korean.
- **Solution:** A full Ukrainian-language site with courses, lessons, a Hangul guide, blog, and news about grants and opportunities in South Korea.
- **Scope:** 10+ pages, 5 courses, free PDF lessons, interactive cart, GDPR-compliant analytics.

---

## 1. UX & Content Writing

- Wrote **100% of interface copy in Ukrainian** across 10+ pages — homepage, courses, lessons, blog, news, reviews, contacts, Hangul guide.
- Created the **Hangul reference page** — a full guide with pronunciation tables, reading rules, and FAQ for beginners.
- Designed **information architecture**: consistent navigation, course cards, cart, favorites.
- Wrote **blog and news content** about grants (GKS-U), exchange programs, and student opportunities.
- Wrote **microcopy** for cart, empty states, error messages, confirmation modals.

### Sample microcopy

| Context | Copy |
|---|---|
| Empty cart | "Кошик порожній" |
| Add to cart success | `"${name}" додано в кошик!` |
| Product already in cart | "Цей товар вже в кошику!" |
| Checkout confirmation | "Підтвердіть покупку на суму ₴..." |
| Purchase success | "🎉 Покупку завершено!" |
| Coming soon page | "Сторінка в розробці" |
| Empty search | "Нічого не знайдено" |

---

## 2. Technical SEO & Audit

Full end-to-end SEO implementation and audit.

### Screaming Frog audit

- Crawled **10+ pages** at launch.
- Verified crawlability of every page — no blocked resources, no orphan pages.
- Confirmed indexability: correct `robots` meta tags, no accidental `noindex`.
- Checked redirect chains — all redirects 301, no loops.

### Issues found & fixed

| Issue | Count | Fix |
|---|---|---|
| Broken internal links | 3 | Updated `href` to correct pages |
| Duplicate titles | 2 | Rewrote unique titles per page |
| Missing canonical | 1 | Added `<link rel="canonical">` |
| Missing `alt` attributes | 4 | Added descriptive alt-text |
| Slow-loading images | 5 | Added `loading="lazy"` + compression |

### On-page SEO (every page)

- **Unique `<title>`** — 50–60 characters
- **Unique `<meta name="description">`** — 150–160 characters
- **`<link rel="canonical">`** — self-referencing
- **H1** — one per page, matching search intent
- **H2–H4** — logical hierarchy, no skipped levels
- **Internal links** — contextual, descriptive anchor text
- **`lang="uk"`** — on `<html>` tag site-wide

### Example metadata

```html
<title>Курси корейської мови TOPIC 1–6 | KORstudy</title>
<meta name="description" content="Курси корейської мови TOPIC 1–6 онлайн. Від початкового до просунутого рівня. Аудіо, PDF, тести, сертифікат. Україномовні матеріали.">
<link rel="canonical" href="https://easy-korean-learning.netlify.app/courses.html">
```

### Structured data (Schema.org)

- **`EducationalOrganization`** — homepage (site-wide identity)
- **`Article`** — Hangul guide page
- **`Course`** — course pages (5 courses)
- Validated with **Rich Results Test**

Example — `EducationalOrganization`:

```json
{
  "@context": "https://schema.org",
  "@type": "EducationalOrganization",
  "name": "KORstudy",
  "url": "https://easy-korean-learning.netlify.app/",
  "logo": "https://easy-korean-learning.netlify.app/img/logoweb.png",
  "contactPoint": {
    "@type": "ContactPoint",
    "email": "studykorwithus@gmail.com",
    "contactType": "customer service",
    "availableLanguage": ["Ukrainian", "Korean"]
  }
}
```

### Social sharing

- **Open Graph** — title, description, image, url, type, locale
- **Twitter Card** — `summary_large_image`
- OG images 1200×630 px, compressed

### Sitemap & robots

**`sitemap.xml`** — all public pages with `lastmod`, `changefreq`, `priority`. Submitted to **Google Search Console**.

**`robots.txt`:**

```
User-agent: *
Allow: /
Disallow: /404.html
Disallow: /coming-soon.html
Disallow: /google07f0eb45ea18c151.html
Disallow: /_redirects

Crawl-delay: 1
Sitemap: https://easy-korean-learning.netlify.app/sitemap.xml
```

### Performance & Core Web Vitals

- **Lazy loading** images below the fold (`loading="lazy"`)
- **Font preconnect** — Google Fonts loaded efficiently
- **Compressed images** — WebP where supported
- **Minimal JS** — vanilla, no heavy frameworks
- **Bootstrap via CDN** — cached across many sites

---

## 3. Development

- **10 responsive HTML5 pages** built with Bootstrap 5.3.
- **Vanilla JavaScript** features:
  - Cart (add, remove, checkout simulation via `localStorage`)
  - Favorites list
  - A/B testing (demo, via `localStorage`)
  - Typewriter effect, filters, carousel, lightbox
- **Clean CSS separation:** `main.css` (typography, layout) + `components.css` (UI components).
- **Mobile-first** design with working burger menu and offcanvas panels.

### File structure

```
korstudy/
├── index.html
├── courses.html
├── lessons.html
├── blog.html
├── news.html
├── reviews.html
├── contacts.html
├── korean-alphabet-hangul.html
├── privacy-policy.html
├── coming-soon.html
├── 404.html
├── robots.txt
├── sitemap.xml
├── _redirects
│
├── css/
│   ├── main.css
│   └── components.css
│
├── js/
│   ├── analytics.js
│   ├── shop.js
│   └── ab-test.js
│
└── img/
```

---

## 4. Privacy & Analytics

- **Google Analytics 4** with **Consent Mode v2** — all trackers blocked by default until consent.
- **CookieYes** — GDPR-compliant consent banner.
- Full **privacy policy** page.
- Custom events tracked: `add_to_cart`, `purchase`, `newsletter_signup`, `contact_form_submit`, `lesson_download`.

---

## 5. Outcome

- ✅ 10+ pages fully in Ukrainian
- ✅ JSON-LD + Open Graph + Twitter Cards
- ✅ Screaming Frog audit passed — 0 SEO errors
- ✅ sitemap.xml + robots.txt live and submitted
- ✅ GA4 + Consent Mode v2 (GDPR)
- ✅ Custom 404 + coming-soon pages
- ✅ Live: [easy-korean-learning.netlify.app](https://easy-korean-learning.netlify.app/)

---

## 6. Skills Demonstrated

**Writing:** UX Writing · Copywriting · Content Strategy · Information Architecture · Microcopy  
**SEO:** Screaming Frog · Google Search Console · Schema.org · JSON-LD · Open Graph · Twitter Cards · sitemap.xml · robots.txt · canonical URLs · meta descriptions · Core Web Vitals  
**Dev:** HTML5 · CSS3 · JavaScript (Vanilla) · Bootstrap 5.3  
**Privacy:** Google Analytics 4 · Consent Mode v2 · GDPR · CookieYes

---

*Built by hand, edited by hand.*
