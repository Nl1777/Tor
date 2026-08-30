# Tor Japan Website — GitHub Pages Setup

This folder contains the full static site: `index.html`, `tours.html`, `about.html`, `faq.html`, `blog.html`, and `booking.html`. No build step needed — it's plain HTML/CSS/JS.

## How to publish on GitHub Pages

1. **Create a new repository** on GitHub (e.g. `tor-japan-site`). Public repos get free Pages hosting; private repos need a paid GitHub plan for Pages.
2. **Upload these files to the root of the repo** (not inside a subfolder) — you can drag-and-drop them on the repo's page via "Add file → Upload files," or push via Git if you're comfortable with that.
3. Go to the repo's **Settings → Pages**.
4. Under "Build and deployment," set **Source** to `Deploy from a branch`, choose the `main` branch and `/ (root)` folder, then **Save**.
5. GitHub will give you a live URL, typically:
   `https://<your-username>.github.io/<repo-name>/`
   It can take a minute or two to go live the first time.
6. **Custom domain (optional):** if you buy a domain (e.g. torjapan.com), add it under the same Pages settings, and create the DNS records GitHub shows you at your domain registrar.

## Notes

- All internal links (nav, footer, buttons) use relative paths like `tours.html`, so they'll work correctly once uploaded — no link changes needed.
- Photo areas are currently color-gradient placeholders. Replace them by swapping the `background` value in the relevant `.tour-photo`, `.blog-photo`, `.strip-card`, or `.hero` CSS rule with a real image, e.g.:
  `background: url('images/higashiyama.jpg') center/cover;`
  (You'd upload an `images/` folder alongside the HTML files for this.)
- The booking form doesn't submit anywhere yet — it just shows a placeholder confirmation. To make it functional, connect it to a form backend (e.g. Formspree, Netlify Forms won't work on GitHub Pages, or a simple email service) or swap it for GitHub Pages–compatible embed of a real booking tool.
