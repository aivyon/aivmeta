# AIVMeta

AIVMeta is a clean, static landing page for an AI media and experimental education brand at **aivmeta.com**. It is built for short AI videos, visual explainers, math and probability micro-lessons, creative workflow notes, and social-first AI storytelling.

## Files

- `index.html` — page content, sections, SEO title, meta description, navigation, social placeholders, and contact CTA.
- `styles.css` — dark visual system, responsive layout, gradient accents, cards, and mobile-first styling.
- `CNAME` — GitHub Pages custom domain configuration for `aivmeta.com`.

## Editing platform links

The platform links are in the `#platforms` section of `index.html`.

Replace each placeholder `href="#"` with the live profile URL when the channel is ready:

```html
<a href="https://www.tiktok.com/@yourhandle" aria-label="AIVMeta on TikTok">TikTok<span>coming soon</span></a>
```

You can also replace the `coming soon` text with a handle, upload cadence, or channel label.

## Updating content series

Content series cards live in the `#series` section of `index.html`. Each card uses this pattern:

```html
<article class="series-card accent-magenta">
  <span class="series-tag">60s</span>
  <h3>AI in 60 seconds</h3>
  <p>Fast, structured explanations of AI ideas with one visual takeaway per clip.</p>
</article>
```

To add or edit a series:

1. Duplicate an existing `series-card`.
2. Update the tag, title, and description.
3. Choose an accent class: `accent-magenta`, `accent-cyan`, `accent-orange`, or `accent-violet`.

## Updating contact details

The contact CTA is in the `#contact` section of `index.html`:

```html
<a class="button button-primary contact-button" href="mailto:hello@aivmeta.com">hello@aivmeta.com</a>
```

Replace the email address with the preferred inbox, form URL, or booking link when available.

## Deploying with GitHub Pages

This site has no framework, no package install, and no build step.

1. Commit changes to the repository.
2. Push the branch to GitHub.
3. In the GitHub repository, open **Settings → Pages**.
4. Set the source to deploy from the desired branch, usually `main`, and the root folder.
5. Confirm the custom domain is set to `aivmeta.com`.
6. Keep the `CNAME` file in the repository root so GitHub Pages preserves the domain setting.

## Local preview

Open `index.html` directly in a browser, or run a simple static server from the repository root:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
