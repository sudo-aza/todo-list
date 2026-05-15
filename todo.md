# Todo List

## Pending

### TTS Testing: Best German Multi-Speaker TTS for CPU (4 vCPU, 8GB RAM, no GPU)

Research completed: see /home/z/repos/workspace/notes/tts-research.md
Results so far: Piper (tts-1) and Kokoro (tts-2) tested successfully, both ~2.9x realtime.

- [ ] **[tts-8] Try CosyVoice (300M model)**
  LLM-based by Alibaba, Apache 2.0 license (commercial OK), German is officially supported. Complex install (clone from source, Python 3.10). Try the 300M model — may be tight on 8 GB RAM. If it fits, generate sample and evaluate quality advantage over lighter options.

- [ ] **[tts-13] Create TTS comparison summary**
  After trying remaining viable engines (or skipping those that don't fit), write a comparison summary to /home/z/repos/workspace/notes/tts-comparison.md. Include: quality ranking, speed benchmark, RAM usage, pros/cons, recommended engine. Send a summary table to Discord. Wait for user to pick their favorite.

## Skipped (research findings)
- ~~[tts-3] MeloTTS~~ — No German support (Issue #145 open, no model released)
- ~~[tts-4] Fish Speech~~ — S2 Pro needs 24 GB VRAM, doesn't fit 4 vCPU / 8 GB RAM
- ~~[tts-5] Coqui XTTS v2~~ — Model download (2GB) exceeds VM disk (10GB total, ~7GB usable). Also requires PyTorch + many deps that fill disk. CPU inference extremely slow (timed out).
- ~~[tts-6] F5-TTS~~ — Requires reference audio for voice cloning (no zero-shot without sample). Would need Piper installed first to generate reference. Heavy PyTorch deps conflict with disk space. CC-BY-NC non-commercial license.
- ~~[tts-7] StyleTTS2~~ — English only, author unresponsive to multilingual requests
- ~~[tts-9] Thorsten-Voice~~ — Voice dataset, not a separate engine. Already covered under Piper TTS
- ~~[tts-10] MMS TTS~~ — Robotic quality + CC-BY-NC 4.0 non-commercial license
- ~~[tts-11] ZeroVOX~~ — pip install fails: readline build error + missing deps (h5py, nemo_text_processing, nltk, lightning). Early alpha quality not worth the dependency pain.
- ~~[tts-12] Bark~~ — Model needs 2.3GB download but only ~7GB usable disk after deps. PyTorch 2.12 weights_only compatibility issue. No space left on device even with small_models=True.

## Done
- [x] 2026-05-11: Set up GitHub account and repos
- [x] 2026-05-11: Create workspace structure and initial journals
- [x] 2026-05-11: Set up cron job for periodic task execution
- [x] 2026-05-11: Add .gitignore to workspace repo
- [x] 2026-05-12: [latex-1] Set up portable LuaLaTeX installation (TeXLive 2026, scheme-basic + 30 packages, /home/z/.texlive/2026)
- [x] 2026-05-12: [latex-2] Create beautiful title page design (dark + light themes, TikZ, 8/10 VLM rating)
- [x] 2026-05-13: [latex-3] Create elegant TOC and sectioning system (titletoc, chapter openers, 9/10 content rating)
- [x] 2026-05-13: [latex-4] Document element templates (tables, lists, code, blockquotes, figures, 8-9/10 VLM rating)
- [x] 2026-05-13: [latex-5] Package everything into sudodoc.sty v1.0.0 (latex-template repo, 8/10 VLM rating)
- [x] 2026-05-14: [analytics] Build progress analytics scripts (matplotlib, 5 plots, git log parsing)
- [x] 2026-05-14: [latex-6] Fix chapter opener pages (sudodoc.sty v1.1.0, newgeometry approach, 8/10 VLM)
- [x] 2026-05-14: [latex-7] Fix TOC width (sudodoc.sty v1.2.0, dotfill leaders, 9/10 VLM)
- [x] 2026-05-14: [latex-8] Fix dark/light mode rendering (sudodoc.sty v1.3.0, theme toggle, 9-10/10 VLM)
- [x] 2026-05-14: [latex-9] Redesign section headings (sudodoc.sty v1.4.0, colored full-width boxes, 9-10/10 VLM)
- [x] 2026-05-14: [tts-research] Research and rank 12 TTS engines for German on CPU. Top 3: Piper+Thorsten, Kokoro, ZeroVOX. 5 engines eliminated (no German or doesn't fit hardware). Findings in notes/tts-research.md.
- [x] 2026-05-15: [tts-1] Try Piper TTS + Thorsten German voice. Installed piper-tts (venv), downloaded high-quality (109 MB) + emotional medium (74 MB, 8 speakers) models. Generated 32s neutral sample in 11s (~2.9x realtime). Tested all 8 emotions. Clear natural German, male only. Install script: scripts/install-piper.sh. Audio sent to Discord.
- [x] 2026-05-15: [tts-2] Try Kokoro-82M German (Martin voice). Installed kokoro-onnx, downloaded community model (311 MB) + voices (511 KB) from huggingFresse. Generated 33.9s German sample in 11.7s (~2.9x realtime). Same speed as Piper, 3x larger model, 1 voice, smoother timbre. Audio sent to Discord.
- [x] 2026-05-15: [tts-blocked] Attempted Coqui XTTS v2, F5-TTS, ZeroVOX, Bark. All blocked by VM constraints: 10GB disk (XTTS 2GB model + PyTorch deps exceed space), dependency build failures (ZeroVOX readline), PyTorch compat issues (Bark), voice cloning requires reference audio (F5-TTS). Only CosyVoice remains to try.
