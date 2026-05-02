# AGENTS.md

## Project Type

Static personal academic website for GitHub Pages.

## Tech Stack

- Plain HTML and CSS.
- No JavaScript runtime.
- No package manager, build tool, framework, or bundler detected.
- Published from the repository root on GitHub Pages.

## Site Structure

- `index.html`: research/home page.
- `cv.html`: CV page.
- `teaching.html`: teaching page.
- `diversity.html`: diversity/service page.
- `contact.html`: contact page.
- `styles.css`: shared stylesheet.
- `assets/cjh_logo_stamp.png`: favicon, brand mark, and homepage emblem.
- `docs/WEBPAGE_HANDOFF.md`: concise handoff context.
- `docs/NEXT_STEPS.md`: future milestone plan.

Each HTML page duplicates the shared header/nav/footer. Keep navigation links and active states synchronized across all pages.

## Coding Conventions

- Use simple static HTML; avoid adding dependencies unless explicitly requested.
- Keep content semantic: `header`, `nav`, `main`, `section`, lists, `address`, and descriptive links.
- Use relative links for internal pages.
- When `styles.css` changes, update the stylesheet query string on every HTML page, e.g. `styles.css?v=YYYYMMDD`, to avoid stale cache.

## Styling Conventions

- Preserve the minimalist academic style.
- Use serif body typography, Garamond-style page titles, small uppercase section labels, thin divider rules, and restrained colors from `:root`.
- Prefer grid/list layouts over cards or decorative blocks.
- Keep pages readable on mobile; existing responsive breakpoint is `860px`.

## Accessibility Expectations

- Maintain meaningful page titles and meta descriptions.
- Keep nav available on every page.
- Ensure links have descriptive text.
- Decorative images should use empty alt text; meaningful linked images need alt text that describes the link purpose.
- Inline SVG icons should remain `aria-hidden` when adjacent text provides the label.

## Do Not Change Without Explicit Instruction

- Published route names: `index.html`, `cv.html`, `teaching.html`, `diversity.html`, `contact.html`.
- The GitHub Pages publishing model from `main` root.
- The academic/minimal visual direction.
- `assets/cjh_logo_stamp.png` usage across favicon, nav, and homepage identity.
- External profile/contact links unless the user provides replacements.

## End-of-Session Summary

Summarize:

- Files changed.
- User-facing behavior or content changed.
- Validation actually performed.
- Whether changes were committed/pushed.
- Any remaining risks or follow-up work.
