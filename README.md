# Zinthora LLC — Company Website

The public website of Zinthora LLC, live at [zinthora.com](https://zinthora.com).

Zinthora builds digital products for digital wellbeing: applications that respect your time
and attention, and are made to leave you calmer rather than to keep you scrolling.

## What is on the page

The site is a single page (`index.html`) with four sections:

| Section | What it shows |
| --- | --- |
| **Home** | The company name, tagline and a short statement of what Zinthora makes |
| **Our Approach** | The six principles the products are built on: calm by design, made to be put down, safe before it reaches you, kind spaces, worth over popularity, respect for your attention |
| **Products** | [Harmony](https://harmony.zinthora.com), a quiet place for short videos — description, screenshots, features and store badges |
| **Contact** | The company address, support email and a contact form |

Harmony is available on
[Google Play](https://play.google.com/store/apps/details?id=com.zinthora.harmony). The App
Store badge is shown as well, and says "Coming soon" when pressed until the app is listed there.

## How it is built

Plain HTML, CSS and JavaScript. There is no build step, no framework and no dependencies to
install.

```
index.html      The page
styles.css      All styling, including the responsive rules
script.js       Mobile menu, smooth scrolling, contact form, screenshot lightbox, store badges
favicon.ico     Kept at the root, where browsers look for it by default
CNAME           The custom domain (zinthora.com)
images/
  icons/        Favicons, touch icon and the Harmony app icon
  logos/        The Zinthora logo
  screenshots/  Harmony screenshots shown on the product card
  *.png         App Store and Google Play badges
```

The only external resources are the Inter typeface from Google Fonts and the form service the
contact form posts to.

## Running it locally

Serve the folder with any static file server, because some image paths are absolute
(`/images/...`) and will not resolve if `index.html` is opened directly as a file:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Making changes

- **Adding a product:** copy the Harmony `product-card` block in `index.html` and put its
  screenshots under `images/screenshots/`. Any image inside `.product-screenshots` opens in the
  lightbox automatically.
- **Listing Harmony on the App Store:** replace the `store-badge-soon` button in `index.html`
  with a link to the listing, the same way the Google Play badge is done.
- **Images:** keep them under `images/`, in the matching subfolder.

## This repository is public

Everything committed here is visible to anyone. Do not commit credentials, API keys, private
contact details or internal documents.

## Contact

[support@zinthora.com](mailto:support@zinthora.com)

&copy; 2026 Zinthora LLC. All rights reserved.
