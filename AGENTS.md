# Repository Guidelines

This repository is a Hugo static site for AirsoftShotTimer, using the PaperMod theme and multilingual content (zh-tw as default, en as secondary).

## Project Structure & Module Organization
- `hugo.toml`: Site configuration, languages, menus, theme options.
- `content/`: Markdown pages and posts (`*.zh-tw.md`, `*.en.md`).
- `layouts/`: Theme overrides and custom templates (e.g., partials, single templates).
- `assets/css/extended/`: Site-specific CSS overrides (e.g., `custom.css`).
- `static/`: Public assets served as-is (e.g., `static/images/...`).
- `themes/PaperMod/`: Upstream theme; avoid editing directly—override via `layouts/` or `assets/`.
- `archetypes/`: Default front matter; posts use TOML front matter (`+++ ... +++`).

## Build, Test, and Development Commands
- `hugo server -D`: Run local dev server with drafts at `http://localhost:1313/`.
- `hugo`: Build the production site into `public/`.
- `hugo --gc --minify`: Clean build with minification; use to validate before PRs.
- Create new post: `hugo new posts/my-post.en.md` (or `.zh-tw.md`).

## Coding Style & Naming Conventions
- Content: Markdown with TOML front matter; title-cased headings, hyphenated slugs.
- Filenames: `kebab-case.language.md` (e.g., `glock-introduction.en.md`).
- Multilingual: Keep content pairs in `content/` with matching slugs and language suffixes.
- Theming: Prefer overrides in `layouts/` and `assets/css/extended/`; do not modify theme files.

## Testing Guidelines
- Build must succeed with `hugo --gc --minify` without warnings.
- For visible changes, paste a local screenshot or attach a Vercel preview URL in the PR.

## Commit & Pull Request Guidelines
- Commits: Imperative, concise messages (e.g., `add zh-tw post: idpa training guide`).
- PRs: Include a clear description, linked issues, and screenshots or preview links for UI changes.
- Scope PRs narrowly (content vs. layout vs. config) and list affected paths (e.g., `content/posts/...`, `layouts/...`).

## Security & Configuration Tips
- Do not commit secrets; configuration belongs in `hugo.toml`. Update menus and language blocks consistently.
- Images: Place under `static/images/...` and reference with absolute paths (e.g., `/images/main/shooter.png`).

請用繁體中文回應使用者