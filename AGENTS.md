# Repository Guidelines

## Project Structure & Module Organization
- Documentation lives in `docs/` with category folders (`features/`, `integrations/`, `api/`, `lunary/`, `more/`); add new `.mdx` files in the matching folder.
- Global navigation stays in `docs.json`; update routes there whenever you add, rename, or reorder pages.
- Store shared assets in `media/docs/` and brand visuals in `logo/`; keep filenames kebab-case and reference them via absolute paths such as `/media/docs/features/analytics.png`.

## Build, Test, and Development Commands
- `npm i -g mintlify` – install or refresh the Mintlify CLI required for local work.
- `mintlify dev` – run the live preview from this directory and confirm tabs from `docs.json` resolve correctly.
- `mintlify install` (when the preview fails) and `mintlify build` (before major releases) – reinstall dependencies and ensure the static bundle compiles locally.

## Coding Style & Naming Conventions
- Start pages with frontmatter (`title`, `icon`, optional `description`) and a concise intro; stick to sentence-case headings.
- Draft content in MDX with a professional voice; use Mintlify components (`<Card>`, `<Callout>`, fenced code blocks) only when they improve comprehension.
- Favor kebab-case filenames, ~100-character lines, two-space list indents, and language-tagged code fences to keep formatting consistent.

## Testing Guidelines
- Preview edits with `mintlify dev`, clicking through navigation tabs to confirm every route and sidebar entry resolves.
- Fix any warnings from the CLI (broken links, invalid frontmatter) before opening a pull request.
- Double-check updated media and code samples in the preview so asset paths, alt text, and runnable snippets stay current with Lunary SDKs.

## Commit & Pull Request Guidelines
- Use the short, imperative style seen in history (e.g., `feat: add evaluations docs`, `fix: sidebar links`) and keep subjects under 72 characters.
- Limit each commit to one focus—content edits, asset updates, or config changes—to simplify reviews and potential rollbacks.
- Pull requests should outline the change, list affected pages, attach screenshots or preview URLs for visual updates, and tag subject-matter reviewers for navigation or API edits.
