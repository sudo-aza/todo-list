# Todo List

## Pending

(no pending tasks — TTS comparison v2 complete)

## Skipped (research findings)
- ~~[tts-3] MeloTTS~~ — No German support (Issue #145 open, no model released)
- ~~[tts-4] Fish Speech~~ — S2 Pro needs 24 GB VRAM, doesn't fit 4 vCPU / 8 GB RAM
- ~~[tts-6] F5-TTS~~ — Requires reference audio for voice cloning (no zero-shot without sample). Would need Piper installed first to generate reference. CC-BY-NC non-commercial license.
- ~~[tts-7] StyleTTS2~~ — English only, author unresponsive to multilingual requests
- ~~[tts-8] CosyVoice 300M~~ — Requires Python 3.10 (ttsfrd has no cp312 wheel). Hard Python blocker.
- ~~[tts-9] Thorsten-Voice~~ — Voice dataset, not a separate engine. Already covered under Piper TTS
- ~~[tts-10] MMS TTS~~ — Robotic quality + CC-BY-NC 4.0 non-commercial license
- ~~[tts-11] ZeroVOX~~ — pip install fails: readline build error + missing deps (h5py, nemo_text_processing, nltk, lightning). Early alpha quality not worth the dependency pain.

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
- [x] 2026-05-15: [tts-1] Try Piper TTS + Thorsten German voice. 32s sample in 11s (~2.9x realtime). 8 emotional speakers. Install: scripts/install-piper.sh.
- [x] 2026-05-15: [tts-2] Try Kokoro-82M German (Martin). 33.9s in 11.7s (~2.9x realtime). 1 voice, 311 MB model.
- [x] 2026-05-15: [tts-blocked] Attempted XTTS v2, F5-TTS, ZeroVOX, Bark. All blocked by constraints.
- [x] 2026-05-15: [tts-13] Created TTS comparison summary at notes/tts-comparison.md (2 engines tested, 10 skipped).
- [x] 2026-05-15: [tts-retry-1] Coqui XTTS v2 RETRIED SUCCESSFULLY. 65 speakers, voice cloning, 0.3-0.8x realtime. CPML license. Install: scripts/install-xtts.sh.
- [x] 2026-05-16: [tts-retry-2] Bark RETRIED AND WORKS. 0.12x realtime (very slow), MIT license, 5.9 GB footprint. Fix: monkey-patch torch.load weights_only=False.
- [x] 2026-05-17: [tts-retry-4] OmniVoice (k2-fsa) tested. 646 languages, voice design mode (no ref audio), female voices, Apache 2.0, 1.0x realtime, 5 GB footprint. Install: PyTorch CPU + omnivoice.
- [x] 2026-05-17: [tts-comparison-v2] Updated notes/tts-comparison.md with all 5 tested engines (Piper, Kokoro, OmniVoice, XTTS v2, Bark). Final ranking: Piper (speed) > OmniVoice (variety) > XTTS v2 (cloning).
