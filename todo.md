# Todo List

## Pending

### TTS Testing: Best German Multi-Speaker TTS for CPU (4 vCPU, 8GB RAM, no GPU)

Research completed: see /home/z/repos/workspace/notes/tts-research.md
Rankings: Piper > Kokoro > ZeroVOX > Bark > CosyVoice > F5-TTS > Coqui XTTS v2
Eliminated: MeloTTS (no DE), StyleTTS2 (no DE), Fish Speech (too heavy), MMS TTS (robotic+NC), Thorsten-Voice (same as Piper)

- [ ] **[tts-2] Try Kokoro TTS German (ONNX model)**
  Community model (huggingFresse/Kokoro-82M-ONNX-German-Martin), 1 male voice "Martin". Install kokoro-onnx, download German model. Generate a German sample, compare to Piper. Send to Discord.

- [ ] **[tts-5] Try Coqui XTTS v2** (was tts-4)
  Abandoned but mature. Supports German (Coqui was German company), zero-shot voice cloning from 6s reference. Non-commercial license (CPML). pip install TTS. Test German with default voice AND try cloning a female voice from reference audio. Note RAM usage and speed on CPU.

- [ ] **[tts-6] Try F5-TTS German fine-tune**
  Diffusion-transformer, 335M params, excellent German fine-tunes (hvoss-techfak/F5-TTS-German on HuggingFace). ~2-3 GB VRAM, fits our hardware. MIT code but CC-BY-NC model weights (non-commercial). pip install f5-tts. Generate sample, note quality vs speed tradeoff.

- [ ] **[tts-8] Try CosyVoice (300M model)**
  LLM-based by Alibaba, Apache 2.0 license (commercial OK), German is officially supported. Complex install (clone from source, Python 3.10). Try the 300M model — may be tight on 8 GB RAM. If it fits, generate sample and evaluate quality advantage over lighter options.

- [ ] **[tts-11] Try ZeroVOX German**
  Ultra-lightweight FastSpeech2, native German+English, pip install zerovox. Early alpha quality but very fast. Zero-shot speaker cloning. Test German output, note quality gap vs heavier models.

- [ ] **[tts-12] Try Bark (Suno) German**
  Expressive generative TTS, MIT license, 100+ speaker presets. pip install suno-bark. Test with small_models=True (6 GB VRAM / 8 GB RAM). Generate German sample, note hallucinations and 13s generation limit.

- [ ] **[tts-13] Create TTS comparison summary**
  After trying all viable engines (or skipping those that don't fit), write a comparison summary to /home/z/repos/workspace/notes/tts-comparison.md. Include: quality ranking, speed benchmark, RAM usage, pros/cons, recommended engine. Send a summary table to Discord. Wait for user to pick their favorite.

## Skipped (research findings)
- ~~[tts-3] MeloTTS~~ — No German support (Issue #145 open, no model released)
- ~~[tts-4] Fish Speech~~ — S2 Pro needs 24 GB VRAM, doesn't fit 4 vCPU / 8 GB RAM
- ~~[tts-7] StyleTTS2~~ — English only, author unresponsive to multilingual requests
- ~~[tts-9] Thorsten-Voice~~ — Voice dataset, not a separate engine. Already covered under Piper TTS
- ~~[tts-10] MMS TTS~~ — Robotic quality + CC-BY-NC 4.0 non-commercial license

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
