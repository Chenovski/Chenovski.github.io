# Webpage Handoff

## Purpose

This repository contains Jinghao Chen's static academic personal website. It presents research interests, academic profile, CV, teaching history, diversity/service activity, and contact information in a minimalist academic style.

## Production Status

The site is published with GitHub Pages at:

https://chenovski.github.io/

Repository remote:

https://github.com/Chenovski/Chenovski.github.io.git

Current publishing model is GitHub Pages from the `main` branch root. The last checked Pages status was `built`.

## Tech Stack

- Static HTML pages
- Plain CSS in a single stylesheet
- No JavaScript runtime
- No package manager, build system, framework, or bundler
- GitHub Pages static hosting

## Important Files and Directories

- `index.html`: research/home page.
- `cv.html`: CV page.
- `teaching.html`: teaching page.
- `diversity.html`: diversity/service page.
- `contact.html`: contact page.
- `styles.css`: shared visual system and responsive layout.
- `assets/cjh_logo_stamp.png`: favicon, brand mark, and homepage identity mark.
- `.nojekyll`: prevents GitHub Pages from applying Jekyll processing.
- `.gitignore`: ignores local tooling, currently `tools/`.
- `README.md`: basic repository and publishing notes.
- `AGENTS.md`: guidance for future Codex sessions.
- `docs/WEBPAGE_HANDOFF.md`: this handoff file.
- `docs/NEXT_STEPS.md`: future milestone plan.

## Page and Component Structure

All pages share the same basic structure:

- `header.site-header`
  - `.brand` link back to `index.html`
  - `.site-nav` with links to Research, CV, Teaching, Diversity, Contact
  - current page marked with `.active`
- `main`
  - page-specific `.page` content
- `footer.site-footer`

Main layout primitives:

- `.research-grid`: homepage research text plus right-side profile facts.
- `.identity`: homepage name/emblem header.
- `.cv-grid`: compact two-column CV summary blocks.
- `.event-list`: three-column event/talk/poster rows.
- `.plain-list`: title plus smaller detail rows.
- `.tag-list`: compact inline tag-like lists.
- `.teaching-year`: grouped teaching entries by academic year.
- `.diversity-grid`: two-column diversity/service layout.
- `.contact-item`: contact rows with inline SVG icons.

## Styling Conventions

The site uses a restrained academic visual language:

- Off-white paper background.
- Serif body typography: Georgia / Times fallback.
- Garamond-style small-caps page titles and name treatment.
- Small uppercase sans-serif labels for section headers.
- Thin divider rules rather than cards or heavy boxes.
- Muted burgundy, green, blue, and gray accents defined as CSS variables in `:root`.
- Responsive CSS collapses grids to one column under `860px`.

Pages currently load:

```html
styles.css?v=20260502
```

The query string is for cache busting. If `styles.css` changes and immediate refresh matters, update this version string on all HTML pages.

## Completed Functionality

- Multi-page navigation instead of a single scrolling page.
- Research is the homepage.
- CV content uses structured compact sections and event rows.
- Teaching entries are grouped by academic year.
- Diversity/service page is renamed to `diversity.html`.
- Contact page includes email and address icons.
- Stamp image has transparent background.
- Site is committed, pushed, and published through GitHub Pages.

## Known Issues or Placeholders

- No tracked `TODO`, `FIXME`, placeholder, `service.html`, or `service-grid` references were found during closeout inspection.
- `tools/` exists locally for portable GitHub CLI use but is ignored and not part of the published site.
- No automated browser, Lighthouse, or accessibility audit is recorded in the repo.

## Deployment Notes

Push changes to `main` on `Chenovski/Chenovski.github.io`. GitHub Pages publishes from the repository root. No build step is needed.

After content or CSS changes:

1. Check local links and layout.
2. Commit changes.
3. Push to `origin main`.
4. Confirm GitHub Pages build status if needed.
5. If CSS changed, update the stylesheet query string to avoid stale browser cache.

## Risks for Future Edits

- Header/footer/nav are duplicated across every HTML page. Page renames or nav changes must be updated manually in all files.
- CSS class names are tightly coupled to HTML layout. Rename classes only with coordinated HTML/CSS updates.
- `styles.css?v=20260502` must remain consistent across pages or cache behavior may differ by route.
- External academic/profile links may change over time.
- The homepage stamp image is used in several roles; replacing it affects favicon, nav, and identity display.
- CV event rows use a three-column layout and can become cramped if entries grow much longer.

## Recommended Next Milestones

- Add a small templating/build workflow to remove duplicated header/footer markup.
- Add Open Graph metadata and a simple sitemap.
- Run visual checks on desktop and mobile browsers.
- Run an accessibility audit and fix any focus, contrast, or link-label issues.
- Consider a dedicated publications page if the publication list grows.
- Consider adding a downloadable CV PDF if desired.
