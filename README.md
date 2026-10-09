# AIVMeta

AIVMeta is a clean, static landing page for an AI media and experimental education brand at **aivmeta.com**. It is built for short AI videos, visual explainers, math and probability micro-lessons, creative workflow notes, and social-first AI storytelling.

## Files

- `index.html` — page content, sections, SEO title, meta description, navigation, social profiles, contact CTA, and visible legal links.
- `privacy.html` — website and Publisher data handling, storage, retention, disconnect behavior, and privacy requests.
- `terms.html` — service terms, authorized accounts, content responsibilities, and third-party platforms.
- `styles.css` — dark visual system, responsive layout, gradient accents, cards, and mobile-first styling.
- `CNAME` — GitHub Pages custom domain configuration for `aivmeta.com`.

## Editing platform links

The platform links are in the `#platforms` section of `index.html`.

The links use the AIVMeta profiles on TikTok, YouTube, and Instagram. Update them only when a profile changes. For example:

```html
<a href="https://www.tiktok.com/@aivmeta" aria-label="AIVMeta on TikTok">TikTok<span>@aivmeta</span></a>
```

Do not add an unverified social profile. Keep both legal links visible in the footer on every public page.

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

This address also receives Publisher support and privacy requests. Keep the address consistent across the homepage and legal pages.

## Maintaining the legal pages

Keep the policies consistent with the actual Publisher implementation. The credential vault uses Windows DPAPI, while publishing metadata and receipts remain separate local records. Disconnecting locally does not delete published content or revoke every platform's access. Review these behaviors before changing the policy and update its effective date for substantive changes.

The public pages are `https://aivmeta.com/privacy.html` and `https://aivmeta.com/terms.html`. Website publication does not establish TikTok app approval; portal configuration, scope eligibility, and app review are separate.

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
