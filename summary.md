# AURELIA — Fine Art Jewelry (Static Website Summary)

A single-page, static marketing website for a fictional luxury jewelry brand called **AURELIA**. It's a demo site (explicitly noted in the footer) built with plain HTML, CSS, and vanilla JavaScript — no frameworks or build tooling.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Page structure and content (plus a `<style>` block for page-specific layout) |
| `styles.css` | Global styles, design tokens, navigation, animations, footer |
| `script.js` | Header scroll effect, scroll-reveal animations, contact form handling |

## Page Sections

1. **Header / Nav** — Fixed top navigation with the AURELIA logo and anchor links (Collection, Experience, Inquire). Becomes opaque with a blur backdrop after scrolling 50px.
2. **Hero** — Full-viewport intro with a background image (Unsplash), tagline "Timeless artifacts for the modern muse," and a "View The Collection" call-to-action button.
3. **The Collection (Gallery)** — A 2-column staggered grid of 4 products (Lumina Gold Band, Celestial Pendant, Ethereal Droplets, Infinite Bangle). Images are placeholder colored blocks (e.g. `[Ring Photo]`) rather than real photos.
4. **Testimonials** — A single italic customer quote attributed to "Eleanor V. Sterling."
5. **Contact (Inquire)** — Two-column layout: brand/atelier contact details (Place Vendôme, Paris) alongside an inquiry form (name, email, interest, message).
6. **Footer** — Logo, social links (Instagram, Pinterest, Journal, Stores), copyright, and a demo-site disclaimer.

## Design

- **Aesthetic:** Minimalist luxury — warm off-white background (`#F5F0EB`), dark text, gold accent (`#C7A86B`).
- **Typography:** Cormorant Garamond (serif headings) + Inter (sans-serif body), loaded from Google Fonts; heavy uppercase letter-spacing.
- **Tokens:** CSS custom properties in `:root` for colors, borders, container width, and a shared slow cubic-bezier transition.
- **Buttons:** `.btn-luxury` with a gold fill that slides in on hover.
- **Responsive:** Single breakpoint at 768px — collapses grids to one column and hides the nav links on mobile.

## JavaScript Behavior

- **Scroll header:** Toggles a `scrolled` class on the header past 50px.
- **Fade-in animations:** `IntersectionObserver` adds a `visible` class to `.fade-in` elements as they enter the viewport.
- **Contact form:** Intercepts submit, shows a "Transmitting inquiry..." state, then after a 2s timeout displays an alert and resets — purely client-side, no backend or data submission.

## Notes / Limitations

- Fully static; no server, backend, or real form submission.
- Product images are placeholder divs, not actual images.
- Mobile nav links are hidden with no hamburger menu replacement (`.nav-toggle` is styled but unused).
- All content is fictional/demo, as stated in the footer.
