# AGENTS.md

## Project Type

Static GitHub Pages site for Jinghao Chen.

The repository contains two distinct sections:

- Formal academic website at the repository root.
- Casual personal side channel under `hanekawa/`.

## Tech Stack

- Plain HTML and CSS.
- No JavaScript runtime.
- No package manager, build tool, framework, or bundler.
- Published from the repository root on GitHub Pages.

## Formal Site Structure

- `index.html`: research/home page.
- `cv.html`: CV page.
- `teaching.html`: teaching page.
- `diversity.html`: diversity/service page and the only formal-page link to the casual section.
- `contact.html`: contact page.
- `styles.css`: formal site stylesheet.
- `assets/cjh_logo_stamp.png`: formal favicon, brand mark, and homepage emblem.

Keep the formal site minimalist and academic. Do not add the casual site to the formal main navigation.

## Casual Site Structure

- `hanekawa/index.html`: casual side-channel home page.
- `hanekawa/styles.css`: casual section stylesheet.
- `hanekawa/posts/index.html`: posts directory and reverse-chronological archive.
- `hanekawa/posts/*.html`: 81 imported post pages.
- `hanekawa/gallery/index.html`: merged gallery.
- `hanekawa/bjj/index.html`: Brazilian Jiu-Jitsu cheatsheet.
- `hanekawa/lineage/index.html`: math lineage page.
- `hanekawa/anime/index.html`: anime recommendation page.
- `hanekawa/resources/index.html`: resources page.
- `hanekawa/assets/media/`: vendored media and document assets.

The casual site has its own visual system: dark, low-profile, lightly stylized, and separate from the formal academic design.

## Coding Conventions

- Use simple static HTML and CSS.
- Keep internal links relative.
- Use explicit `index.html` links in the casual nav, e.g. `bjj/index.html`, because the site is often previewed directly from files.
- Header/nav/footer markup is duplicated across both the formal pages and the casual pages; update all affected pages when changing shared navigation.
- If `styles.css` changes, update the formal stylesheet query string on all formal HTML pages.
- If `hanekawa/styles.css` changes and cache busting matters, update the casual stylesheet query string on all casual HTML pages.

## Accessibility Expectations

- Maintain meaningful page titles and meta descriptions.
- Keep navigation available on every page.
- Use descriptive link text.
- Decorative images should have empty alt text; linked or meaningful images need useful alt text.

## Do Not Change Without Explicit Instruction

- Published formal route names: `index.html`, `cv.html`, `teaching.html`, `diversity.html`, `contact.html`.
- GitHub Pages publishing from `main` branch root.
- Formal academic visual direction.
- The casual site’s separation from the formal navigation.
- Vendored casual media paths under `hanekawa/assets/media/`.
- External profile/contact links unless replacements are provided.

## End-of-Session Summary

Summarize:

- Files changed.
- User-facing behavior or content changed.
- Validation actually performed.
- Whether changes were committed/pushed.
- Remaining risks or follow-up work.
