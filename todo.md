# Todo List

## 🔲 Pending

- [ ] **[analytics] Build progress analytics scripts**
  Write scripts in /home/z/repos/workspace/scripts/analytics/ that track and visualize: total LOC across repos, todo count (pending vs done) over time, tasks completed per maintenance run, repo growth over time. Use matplotlib for plots. Read git log and todo.md history. Save plots as PNGs, send to Discord. This task depends on having activity data — do NOT start before May 13th 2026.

---

### TTS Research: Best German Multi-Speaker TTS for CPU (4 vCPU, 8GB RAM, no GPU)

Requirements: German language, multi-speaker (or at least multiple voice options), not monotonous, runs on CPU-only hardware, open source, best possible quality.

- [ ] **[tts-research] Research and rank all viable TTS engines for German on CPU**
  Do a deep-dive web research on every TTS engine that could possibly run on this hardware (4 vCPU, 8GB RAM, no GPU). For each engine, check: (1) German language support, (2) multiple voices/speakers, (3) prosody and naturalness quality, (4) CPU RAM/speed requirements, (5) license, (6) installation complexity. Candidates to investigate thoroughly (not limited to): Piper TTS (thorsten voice), Coqui XTTS v2, Fish Speech, Kokoro (German ONNX models exist), MeloTTS, CosyVoice, F5-TTS (German fine-tune), StyleTTS2, Thorsten-Voice (native German), MMS TTS (Meta), ZeroVOX, Bark, Mimic3, Glow-TTS. Write findings to /home/z/repos/workspace/notes/tts-research.md. Rank engines by quality-feasibility on our hardware. Add individual try-todos for every engine that is viable.

- [ ] **[tts-1] Try Piper TTS with Thorsten German voice**
  Piper is lightweight ONNX-based TTS, fast on CPU. Thorsten is a high-quality German voice model. Install piper-tts, download German voice models (thorsten medium/high quality, possibly multiple voices). Generate a ~30s German sample with natural prosody (a short story or dialogue). Send WAV/MP3 to Discord. Note quality, speed, and naturalness.

- [ ] **[tts-2] Try Kokoro TTS German (ONNX model)**
  Kokoro has a German ONNX model (Kokoro-82M-ONNX-German-Martin by FuggingFresse on HuggingFace). Very small model (82M), should be fast on CPU. Install kokoro or use the ONNX runtime directly. Generate a German sample. Send to Discord.

- [ ] **[tts-3] Try MeloTTS German**
  MeloTTS by MyShell.ai — fast enough for real-time CPU inference. Check if German language pack is available (it supports EN, ZH, JP, KR — German may need a community addon). If German is available, install and generate a sample. If no German support exists, skip and note in research.

- [ ] **[tts-4] Try Fish Speech (fish-speech)**
  Fish Speech — SOTA open source multilingual TTS. Supports many languages including German. Uses LLM-based architecture. Check if the smaller model can run on 8GB CPU. Install, configure for German, generate a sample with a natural/expressive voice. May be slow on CPU but quality should be excellent.

- [ ] **[tts-5] Try Coqui XTTS v2**
  Coqui XTTS v2 — supports 17 languages including German, zero-shot voice cloning, multi-speaker. Can be heavy on CPU (may need quantization or smaller settings). Install TTS package, try German with default and cloned voices. Generate sample. Note if 8GB RAM is sufficient.

- [ ] **[tts-6] Try F5-TTS German fine-tune**
  F5-TTS is a diffusion-transformer based TTS. There is a German fine-tuned model on HuggingFace by tabularisai. Check CPU requirements, install, generate a German sample. Diffusion models are typically slow on CPU but quality may be worth it.

- [ ] **[tts-7] Try StyleTTS2**
  StyleTTS2 — aims for human-level TTS using style diffusion and adversarial training. Check if it supports German (originally EN-focused). If German works or can be adapted, install and test. Requires significant RAM — may not fit in 8GB. Document findings.

- [ ] **[tts-8] Try CosyVoice**
  CosyVoice by Alibaba — multi-lingual LLM-based TTS. Check if it supports German (9 languages + 18 dialects listed). If German is available, try running on CPU. Likely very heavy (LLM-based) — may not fit on 8GB RAM without quantization.

- [ ] **[tts-9] Try Thorsten-Voice (native German TTS)**
  Thorsten-Voice is a dedicated German TTS project with multiple models for Coqui/Piper. Check what backend options exist beyond Piper (the tts-research + tts-1 may overlap). If there are standalone thorsten models for other backends, try those. Generate a German sample.

- [ ] **[tts-10] Try MMS TTS (Meta) German**
  Meta's Massively Multilingual Speech (MMS) TTS — supports 1100+ languages including German. Very lightweight, designed for low-resource. Install via transformers, generate a German sample. Quality may be basic but worth comparing as baseline.

- [ ] **[tts-11] Try ZeroVOX German**
  ZeroVOX — FastSpeech2-based with zero-shot speaker cloning. Claims real-time CPU and embedded use. Check German language support. If available, install via pip (zerovox), generate a German sample.

- [ ] **[tts-12] Try Bark (Suno) German**
  Bark by Suno — multilingual TTS with expressive/narrative capabilities. Supports German. Can be slow on CPU and produces long-form audio. Install, generate a short expressive German sample. Note quality vs speed tradeoff.

- [ ] **[tts-13] Create TTS comparison summary**
  After trying all viable engines (or skipping those that don't support German / don't fit hardware), write a comparison summary to /home/z/repos/workspace/notes/tts-comparison.md. Include: quality ranking, speed benchmark, RAM usage, pros/cons, recommended engine. Send a summary table to Discord. Wait for user to pick their favorite.

## ✅ Done
- [x] 2026-05-11: Set up GitHub account and repos
- [x] 2026-05-11: Create workspace structure and initial journals
- [x] 2026-05-11: Set up cron job for periodic task execution
- [x] 2026-05-11: Add .gitignore to workspace repo
- [x] 2026-05-12: [latex-1] Set up portable LuaLaTeX installation (TeXLive 2026, scheme-basic + 30 packages, /home/z/.texlive/2026)
- [x] 2026-05-12: [latex-2] Create beautiful title page design (dark + light themes, TikZ, 8/10 VLM rating)
- [x] 2026-05-13: [latex-3] Create elegant TOC and sectioning system (titletoc, chapter openers, 9/10 content rating)
- [x] 2026-05-13: [latex-4] Document element templates (tables, lists, code, blockquotes, figures, 8-9/10 VLM rating)
- [x] 2026-05-13: [latex-5] Package everything into sudodoc.sty v1.0.0 (latex-template repo, 8/10 VLM rating)
