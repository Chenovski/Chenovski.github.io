# Next Steps

## Milestone 1: Remove Repeated Header and Footer Markup

- **Goal:** Introduce a lightweight templating or generation workflow so shared nav/header/footer markup is edited in one place.
- **Why it matters:** Every page currently duplicates navigation and footer HTML, which makes route renames and nav changes easy to miss.
- **Likely files affected:** `index.html`, `cv.html`, `teaching.html`, `diversity.html`, `contact.html`, possibly a new template/source directory and README updates.
- **Acceptance criteria:** All pages render the same content and navigation as before; shared header/footer can be updated from one source.
- **Avoid changing:** Published route names, visual design, existing page content unless explicitly requested.
- **Validation/manual review:** Compare all pages before and after generation; verify nav active states; open each page locally and after deployment.

## Milestone 2: Improve SEO and Social Metadata

- **Goal:** Add better metadata for search engines and link previews.
- **Why it matters:** Current pages have basic titles and descriptions but no canonical links, Open Graph tags, sitemap, or structured data.
- **Likely files affected:** All HTML pages, possible new `sitemap.xml` and `robots.txt`.
- **Acceptance criteria:** Each page has appropriate title, description, canonical URL, and social preview metadata; sitemap lists all public pages.
- **Avoid changing:** Visible page copy unless needed for metadata consistency and approved by the user.
- **Validation/manual review:** Inspect page source; test link previews where practical; verify sitemap URLs match deployed routes.

## Milestone 3: Accessibility Audit and Fixes

- **Goal:** Review and improve keyboard navigation, link labeling, image alt text, heading order, and contrast.
- **Why it matters:** The site is simple but has linked images, repeated nav, muted colors, and custom layout patterns that should be checked.
- **Likely files affected:** HTML pages, `styles.css`, possibly `assets/cjh_logo_stamp.png` usage.
- **Acceptance criteria:** Keyboard navigation is clear; meaningful images and links have useful labels; heading structure is logical; contrast passes normal text expectations.
- **Avoid changing:** Overall minimalist style, content wording, or page structure beyond accessibility fixes.
- **Validation/manual review:** Manual keyboard pass; browser accessibility tree inspection; automated audit if available.

## Milestone 4: Visual QA Across Viewports

- **Goal:** Verify and refine layout across common desktop, tablet, and mobile widths.
- **Why it matters:** CV event rows and diversity grids can become cramped as content grows.
- **Likely files affected:** `styles.css`, possibly long text in `cv.html` or `diversity.html`.
- **Acceptance criteria:** No overlapping text; nav wraps cleanly; event rows remain readable; grids collapse properly under the mobile breakpoint.
- **Avoid changing:** Academic color palette and typography unless a layout issue requires a small adjustment.
- **Validation/manual review:** Screenshots or manual checks at desktop, tablet, and phone widths; inspect `cv.html` and `diversity.html` especially.

## Milestone 5: Expand Publications and Research Output

- **Goal:** Add a scalable publications/research-output section or separate page if the publication list grows.
- **Why it matters:** The homepage currently contains one featured publication; future output may need a more structured format.
- **Likely files affected:** `index.html`, possibly new `publications.html`, `styles.css`, shared navigation.
- **Acceptance criteria:** Publications are easy to scan, consistently formatted, and linked to DOI/preprint/journal pages where available.
- **Avoid changing:** Existing featured publication wording unless updating bibliographic details.
- **Validation/manual review:** Check citation formatting, links, wrapping, and mobile readability.

## Milestone 6: Add Downloadable CV

- **Goal:** Add a downloadable PDF CV link if the user wants a formal document version.
- **Why it matters:** Academic visitors often expect a downloadable CV alongside the web CV.
- **Likely files affected:** `cv.html`, `assets/` or a new `files/` directory, possibly `styles.css`.
- **Acceptance criteria:** CV PDF is linked clearly from the CV page; file opens/downloads correctly; visible web CV remains unchanged unless requested.
- **Avoid changing:** Web CV content without checking against the source PDF or user instructions.
- **Validation/manual review:** Open the PDF from the deployed site; verify file size and link target.

## Milestone 7: Content Freshness Review

- **Goal:** Periodically update appointments, awards, talks, posters, teaching history, memberships, and contact details.
- **Why it matters:** Academic pages become stale quickly, especially CV and conference information.
- **Likely files affected:** `index.html`, `cv.html`, `teaching.html`, `diversity.html`, `contact.html`.
- **Acceptance criteria:** New content is accurate, dated consistently, and fits current layout without visual overflow.
- **Avoid changing:** Historical entries unless the user explicitly corrects them.
- **Validation/manual review:** User review for factual accuracy; link checks for new external references.
