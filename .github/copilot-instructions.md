# Copilot / AI agent instructions for desafio-listagem-youtube-css ✅

## Project summary
- Small, static single-page HTML/CSS project that replicates a YouTube-like layout.
- Key files: `index.html`, `assets/css/style.css`, `assets/css/reset.css`, and `assets/images/`.
- No JS, build system, or automated tests in this repository.

## Big picture / intent 💡
- Purpose: CSS layout challenge / UI exercise. The primary work is visual: structure, spacing, responsive behavior.
- Layout implemented with CSS Grid on `body` (two columns, header row and main content). Header, `aside` and `main` are the main regions.

## Important files and patterns (reference examples) 🔧
- `index.html` — structure: header/nav, `main`, and `aside`. Sidebar items are simple `div` blocks with `img` and `p`.
  - Example sidebar item:
    ```html
    <div id="explorar">
      <img src="assets/images/compass.png">
      <p>Explorar</p>
    </div>
    ```
- `assets/css/style.css` — imports `reset.css`, sets `font-family: Roboto`, defines `body` grid:
  - `grid-template-columns: 1fr 5fr;` and `grid-template-areas: "header header" "aside main";`
- Image filenames include spaces/parentheses (e.g., `menu (1).png`). Be careful when modifying or serving—they may require URL encoding or renaming with updates to references.
- Paths in HTML currently use leading slashes (`/assets/images/...`) — when previewing via file:// this can break. Prefer relative paths (`assets/images/...`) for portability.

## Developer workflows ⚙️
- No build step: to preview changes open `index.html` in a browser or use a static server (e.g., VS Code Live Server extension).
- Debugging/CSS tweaks: use browser DevTools, tweak `assets/css/style.css` and refresh.
- When making visual changes, rely on quick manual validation across screen widths (no responsive test harness present).

## Common modifications — concrete guidance ✅
- Add a sidebar item: append a new `<div id="...">...</div>` inside `<aside>` and add styling (if necessary) in `assets/css/style.css`.
- Adjust page grid: edit `grid-template-columns` and `grid-template-areas` in `body` in `style.css`.
- Rename image files: update all `src` references in `index.html` (search for the filename first).

## Safety rules for agents (must follow) ⚠️
- Do not introduce a build system, test framework, or dependencies without explicit approval from the repo owner.
- Avoid mass renames of image files or breaking absolute paths—prefer safe fixes like converting leading `/assets/...` → `assets/...`.
- Keep PRs minimal and visually verifiable (e.g., one visual change per PR) and include screenshots or steps to reproduce preview.

## Questions to ask the maintainer (if uncertain) ❓
- Should image filenames be normalized (no spaces) and references updated across the repo?
- Is responsive layout intended beyond the current desktop grid? If so, where should mobile styles live (same `style.css` or a new file)?

---
If anything here is unclear or you'd like more detail (examples for responsive patterns, naming conventions, or an initial issue template), tell me what to add and I'll iterate. ✨