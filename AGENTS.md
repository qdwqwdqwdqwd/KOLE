# Repository Guidelines

Use these guardrails to keep documentation changes consistent and auditable.

## Project Structure & Module Organization
- `docs/` hosts the bilingual whitepaper and community guides. Update English and Chinese counterparts in tandem and refresh tables of contents after structural edits.
- `data/知识库.json` stores canonical release metadata. Keep keys ordered, bump `metadata_version`, and mirror version strings with the whitepaper headers.
- `CLAUDE.md` and `AGENTS.md` document agent workflows; keep shared policies aligned when either file changes.
- `.env` supports local experiments only. Replace live tokens with placeholders before committing and document required variables in PR notes.

## Build, Test, and Development Commands
- `npx markdownlint-cli README.md docs/**/*.md` checks Markdown headings, lists, and links.
- `jq '.' data/知识库.json` validates JSON syntax before raising a pull request.
- `python -m http.server 8000` (from the repo root) previews Markdown rendering in a browser; stop with `Ctrl+C`.

## Coding Style & Naming Conventions
- Prefer ATX headings (`#`, `##`) with one blank line around blocks; use bolded lists sparingly to match the existing whitepaper tone.
- Keep two-space indentation in JSON and snake_case keys (e.g., `last_updated`). Dates follow `YYYY-MM` or ISO-8601 as shown in current entries.
- Title Case English filenames and simplified Chinese names for localized content; mirror naming when adding translation pairs.

## Testing Guidelines
- Run the Markdown and JSON checks above before every push.
- Cross-check version strings and release dates between the whitepaper titles and `data/知识库.json`.
- When adding community procedures, include an example or table to stay consistent with current documentation.

## Commit & Pull Request Guidelines
- Follow the Git history convention: imperative mood, ≤72 characters (e.g., `Add community reward rubric`). Reference issue IDs inline when available.
- PRs summarize the change, list affected files, note validation commands, and call out localization follow-ups if needed.
- Attach screenshots only when UI mockups change; otherwise link to the affected document section.

## Security & Configuration Tips
- Never publish operational secrets; rotate any leaked token immediately and note the response in the PR.
- If a new environment variable is required, add a masked example to `.env` and explain its purpose in the PR description.
