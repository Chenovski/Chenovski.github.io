# Webpage Handoff

## Current State

This repository is the published GitHub Pages site for Jinghao Chen:

- Production URL: https://chenovski.github.io/
- Repository: https://github.com/Chenovski/Chenovski.github.io.git
- Publishing model: `main` branch, repository root.
- Latest inspected commit: `b974112 Built a side channel`.

The working tree was clean before this documentation closeout.

## Site Sections

### Formal Academic Site

Root-level pages:

- `index.html`: research/home page.
- `cv.html`: CV page.
- `teaching.html`: teaching page.
- `diversity.html`: diversity/service page.
- `contact.html`: contact page.

Shared formal assets:

- `styles.css`
- `assets/cjh_logo_stamp.png`

The formal site keeps a minimalist academic style: off-white paper background, serif typography, restrained color accents, thin divider rules, compact academic lists, and no JavaScript.

`diversity.html` contains the only formal-site link into the casual section.

### Casual Side Channel

Route:

- `hanekawa/index.html`

Main casual pages:

- `hanekawa/posts/index.html`
- `hanekawa/gallery/index.html`
- `hanekawa/bjj/index.html`
- `hanekawa/lineage/index.html`
- `hanekawa/anime/index.html`
- `hanekawa/resources/index.html`

Content inventory:

- 81 imported individual post pages under `hanekawa/posts/`.
- 187 vendored files under `hanekawa/assets/media/`.
- Vendored media size is about 144.48 MiB.
- Total `hanekawa/` size is about 144.77 MiB.

The casual site uses `hanekawa/styles.css` and a dark, low-profile visual style. It is intentionally separate from the formal nav. Casual pages include a footer link back to the formal site.

## Navigation Notes

- Formal nav appears only on root-level formal pages.
- Casual nav appears only inside `hanekawa/`.
- Casual nav uses explicit `index.html` links for direct file-preview compatibility.
- Header/nav/footer markup is duplicated manually.

## Validation Notes

Recent validation performed during the build:

- Local relative link scan across 93 HTML files passed.
- Casual media URLs were vendored locally; old `sites.uci.edu/.../files` media references were removed.
- WordPress gallery/video/caption shortcodes were converted or removed from rendered pages.
- No JavaScript or dependencies were added.

No browser, Lighthouse, or accessibility audit is recorded.

## Deployment Notes

No build step is required. To deploy future changes:

1. Review local diff.
2. Run a local relative-link scan.
3. Commit changes on `main`.
4. Push to `origin main`.
5. Confirm GitHub Pages build if needed.

If either stylesheet changes and browser cache matters, update the corresponding query strings:

- Formal pages: `styles.css?v=...`
- Casual pages: `hanekawa/styles.css?v=...` as referenced from each casual HTML file.

## Risks and Maintenance Notes

- Manual duplicated navigation is the main maintenance risk.
- The casual section contains many generated/imported static pages; broad hand edits are easy to miss across the archive.
- Vendored media is large enough to matter for repository size, though the largest file was previously under GitHub’s 100 MiB single-file limit.
- The formal and casual visual systems should remain separate unless explicitly requested.
