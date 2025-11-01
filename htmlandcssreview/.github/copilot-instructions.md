## Purpose
Help AI coding assistants be immediately productive in this repository: a small static HTML/CSS review site located in `htmlandcssreview/`.

Keep suggestions tightly scoped to the repository layout and minimal toolchain (no build system detected).

## Big picture
- This is a static-site exercise repo. Key content lives under `htmlandcssreview/`.
- Major folders:
  - `htmlandcssreview/` — repo root for the site.
  - `htmlandcssreview/css/` — CSS files (stylesheets that style the HTML).
  - `htmlandcssreview/images/` — static image assets.
  - `htmlandcssreview/index.html` — the site entrypoint (a minimal `index.html` file has been added). It links to `css/style.css`.

Why this structure: everything is served statically. There is no JS build, package.json, or server framework in the repository.

## What to look for first (quick checklist)
- Confirm `htmlandcssreview/index.html` exists and that the `<link rel="stylesheet" href="css/style.css">` reference points to an existing stylesheet in `css/`.
- Open any `.html` files under `htmlandcssreview/` and the `.css` files in `htmlandcssreview/css/` to understand current markup and selectors.
- Keep paths relative: HTML references to CSS and images should be like `css/<name>.css` and `images/<name>.png`.

## How to run / preview locally
Use a lightweight static server from the `htmlandcssreview/` directory. Example (macOS / zsh):

```bash
cd htmlandcssreview
python3 -m http.server 8000
# then open http://localhost:8000 in your browser
```

Alternatively, use VS Code Live Server to preview edits live.

## Project-specific conventions and patterns
- No frontend framework: changes should be made directly to HTML/CSS files.
- Keep styles in `css/` and assets in `images/` — do not introduce new build steps or bundlers.
- Favor semantic HTML where practical; follow existing naming patterns in `css/` selectors.

## Integration points & external dependencies
- There are no external integrations or package manifests detected (no `package.json`, no `requirements.txt`). Assume a plain static site.

## Examples for common tasks
-- To fix a broken image path referenced from `htmlandcssreview/index.html`:
  - Open `htmlandcssreview/index.html`.
  - Ensure the <img> `src` points to `images/<filename>` and that the file exists under `htmlandcssreview/images/`.

-- To add/modify styles:
  - Edit `htmlandcssreview/css/style.css` (created as a baseline) or create additional css files under `css/` and update the `<link rel="stylesheet" href="css/<name>.css">` line in the HTML head.

## Editing guidance for AI agents
- Make minimal, focused changes and include a short explanation comment in PRs or commits describing why the edit was made (e.g., "fix missing index.html file" or "adjust header padding to match design").
- If the repository lacks an `index.html` file but has an `index.html/` directory (as currently present), create the file instead of editing the directory; call this out in the change.
- When proposing structural changes (new folders, build tools), first ask whether such a change is acceptable — this repo is intentionally minimal.

## Files to reference
- `htmlandcssreview/README.md` — repo-level information (currently minimal).
- `htmlandcssreview/css/` — stylesheets.
- `htmlandcssreview/images/` — images and static assets.

## When you can't find something
- If an expected file (for example, `index.html`) is missing, prefer adding a short, explicit TODO comment in the code and open a PR describing the missing artifact and proposed fix.

---
If anything here is unclear or you want the instructions to be tighter (for example, include exact filenames that should exist), tell me which areas to expand and I will update this file.
