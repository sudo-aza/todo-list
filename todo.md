# Todo List

## 🔲 Pending

- [ ] **[latex-1] Set up portable LuaLaTeX installation**
  Download and install TeXLive portable (minimal + required packages) to /home/z/repos/workspace/texlive/. Ensure `lualatex` is on PATH or accessible via wrapper script. Packages needed: fontspec, geometry, titlesec, tocloft, booktabs, enumitem, xcolor, graphicx, hyperref, microtype, koma-script or memoir, tikz, calc, etoolbox.

- [ ] **[latex-2] Create beautiful title page design**
  Design a title page inspired by the Typst Thesis Starter aesthetic: clean, minimalist, modern with strong typographic hierarchy. Should support title, subtitle, author, date, institution, and optional logo/decorative rule. Use the LuaLaTeX setup from latex-1. Render a test PDF and verify with VLM that it looks good.

- [ ] **[latex-3] Create elegant TOC and sectioning system**
  Build a TOC with clean formatting, dotted leaders, and proper chapter/section/subsection hierarchy. Style headings consistently with the title page design. Include custom chapter pages (optional decorative elements on chapter openers).

- [ ] **[latex-4] Create document element templates (tables, lists, figures, code)**
  Build beautiful templates for: tables (booktabs-style, alternating row colors), ordered/unordered lists (custom bullets/numbers, proper spacing), figure environments with captions, code listings (with syntax highlighting if possible), blockquotes, and definition/description lists. Each should be configurable and match the overall document style.

- [ ] **[latex-5] Package everything into an easily importable config**
  Consolidate all the above into a single `\input{}`-able or `\usepackage{}`-style LaTeX config file (e.g. `sudodoc.sty` or `sudodoc.tex`). Write a sample document that demonstrates all features (title page, TOC, chapters, tables, lists, code blocks). Render final sample PDF and verify with VLM. Push everything to a `latex-template` repo on GitHub.

- [ ] **[analytics] Build progress analytics scripts — DO NOT START BEFORE 2026-05-13**
  Write scripts in /home/z/repos/workspace/scripts/analytics/ that track and visualize: total LOC across repos, todo count (pending vs done) over time, tasks completed per maintenance run, repo growth over time. Use matplotlib for plots. Read git log and todo.md history. This task depends on having some activity data, so do NOT start before May 13th 2026.

## ✅ Done
- [x] 2026-05-11: Set up GitHub account and repos
- [x] 2026-05-11: Create workspace structure and initial journals
- [x] 2026-05-11: Set up cron job for periodic task execution
