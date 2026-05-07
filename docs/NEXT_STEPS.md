# Next Steps

## Milestone 1: Visual QA

- **Goal:** Review the formal and casual pages across desktop, tablet, and mobile widths.
- **Why it matters:** Both sections use manually maintained responsive CSS, and the casual home/gallery pages contain large visual assets.
- **Likely files affected:** `styles.css`, `hanekawa/styles.css`, possibly individual HTML pages if text or image layout needs adjustment.
- **Acceptance criteria:** No overlapping text, broken wrapping, cropped important content, or incoherent navigation layout.
- **Avoid changing:** Formal/casual design separation and existing route names.
- **Validation:** Browser screenshots or manual checks at common viewport widths.

## Milestone 2: Accessibility Pass

- **Goal:** Check heading order, keyboard navigation, alt text, focus visibility, link labels, and contrast.
- **Why it matters:** The site is static, but both sections use custom layout and many imported media links.
- **Likely files affected:** HTML pages and CSS files.
- **Acceptance criteria:** Pages remain navigable by keyboard, meaningful images and links are labeled, and text contrast is acceptable.
- **Avoid changing:** Visible content tone unless needed for accessibility.
- **Validation:** Manual keyboard pass plus automated accessibility scan if available.

## Milestone 3: Reduce Duplicated Navigation

- **Goal:** Consider a lightweight static generation workflow for shared headers, nav, and footers.
- **Why it matters:** Navigation is duplicated across formal pages and many casual pages.
- **Likely files affected:** All HTML pages, possible new source/template files, documentation.
- **Acceptance criteria:** Rendered output remains visually unchanged while shared nav can be updated from one source.
- **Avoid changing:** GitHub Pages root publishing model unless explicitly approved.
- **Validation:** Compare generated pages, active states, and local links.

## Milestone 4: Metadata and Sitemap

- **Goal:** Add canonical URLs, Open Graph metadata, `sitemap.xml`, and `robots.txt`.
- **Why it matters:** The site has multiple public sections but limited social/search metadata.
- **Likely files affected:** HTML pages, new `sitemap.xml`, new `robots.txt`.
- **Acceptance criteria:** Public routes are represented accurately and link previews have appropriate titles/descriptions.
- **Avoid changing:** Visible page content unless explicitly approved.
- **Validation:** Inspect page source and verify sitemap routes.

## Milestone 5: Casual Archive Maintenance

- **Goal:** Review the imported casual archive for broken external links, outdated resources, and oversized media.
- **Why it matters:** The casual section includes 81 imported posts and 187 vendored media files.
- **Likely files affected:** `hanekawa/posts/`, `hanekawa/resources/index.html`, `hanekawa/assets/media/`.
- **Acceptance criteria:** Local media remains present, external resources are either still valid or clearly marked, and repository size remains manageable.
- **Avoid changing:** Original individual post bodies unless the user explicitly requests edits.
- **Validation:** Link check and media-size report.

## Milestone 6: Formal Content Freshness

- **Goal:** Periodically update appointments, publications, talks, teaching history, service, and contact details.
- **Why it matters:** Academic pages become stale quickly.
- **Likely files affected:** `index.html`, `cv.html`, `teaching.html`, `diversity.html`, `contact.html`.
- **Acceptance criteria:** New information is accurate, dated consistently, and fits the current layout.
- **Avoid changing:** Historical entries without explicit correction.
- **Validation:** User factual review and local layout check.
