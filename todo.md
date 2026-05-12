# Todo List

## 🔲 Pending

- [ ] **[latex-2] Create beautiful title page design**
  Design a title page inspired by the Typst Thesis Starter aesthetic: clean, minimalist, modern with strong typographic hierarchy. Should support title, subtitle, author, date, institution, and optional decorative rule/line. Use the LuaLaTeX setup from latex-1. Render a test PDF, convert the title page to PNG (use `pdftoppm` or `convert`), and send the PNG to Discord via send_message for preview. Verify visually.

- [ ] **[latex-3] Create elegant TOC and sectioning system**
  Build a TOC with clean formatting, dotted leaders, and proper chapter/section/subsection hierarchy. Style headings consistently with the title page design. Include custom chapter pages (decorative elements on chapter openers). Render a test PDF with sample chapters, convert key pages to PNG, send to Discord for preview.

- [ ] **[latex-4] Create document element templates (tables, lists, figures, code)**
  Build beautiful templates for: tables (booktabs-style, alternating row colors), ordered/unordered lists (custom bullets/numbers, proper spacing), figure environments with captions, code listings (syntax highlighting), blockquotes, and definition/description lists. Each should match the overall document style. Render test pages, convert to PNG, send to Discord.

- [ ] **[latex-5] Package everything into an importable config**
  Consolidate all the above into a single `\input{}`-able or `\usepackage{}`-style file (e.g. `sudodoc.sty`). Write a sample document demonstrating all features (title page, TOC, chapters, tables, lists, code blocks). Render final sample PDF, convert all pages to PNGs, send key pages to Discord. Create a `latex-template` repo on GitHub and push the .sty, sample doc, and install script there.

- [ ] **[analytics] Build progress analytics scripts — DO NOT START BEFORE 2026-05-13**
  Write scripts in /home/z/repos/workspace/scripts/analytics/ that track and visualize: total LOC across repos, todo count (pending vs done) over time, tasks completed per maintenance run, repo growth over time. Use matplotlib for plots. Read git log and todo.md history. Save plots as PNGs, send to Discord. This task depends on having activity data — do NOT start before May 13th 2026.

## ✅ Done
- [x] 2026-05-11: Set up GitHub account and repos
- [x] 2026-05-11: Create workspace structure and initial journals
- [x] 2026-05-11: Set up cron job for periodic task execution
- [x] 2026-05-11: Add .gitignore to workspace repo
- [x] 2026-05-12: [latex-1] Set up portable LuaLaTeX installation (TeXLive 2026, scheme-basic + 30 packages, /home/z/.texlive/2026)
