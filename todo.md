# Todo List

## Pending

(no pending tasks — TTS retry evaluation complete)

## Skipped (research findings)
- ~~[tts-3] MeloTTS~~ — No German support (Issue #145 open, no model released)
- ~~[tts-4] Fish Speech~~ — S2 Pro needs 24 GB VRAM, doesn't fit 4 vCPU / 8 GB RAM
- ~~[tts-5] Coqui XTTS v2~~ — ~~Model download (2GB) exceeds VM disk~~ RETRIED AND WORKS. See tts-retry-1.
- ~~[tts-6] F5-TTS~~ — Requires reference audio for voice cloning (no zero-shot without sample). Would need Piper installed first to generate reference. CC-BY-NC non-commercial license.
- ~~[tts-7] StyleTTS2~~ — English only, author unresponsive to multilingual requests
- ~~[tts-8] CosyVoice 300M~~ — Requires Python 3.10 (ttsfrd has no cp312 wheel). Hard Python blocker.
- ~~[tts-9] Thorsten-Voice~~ — Voice dataset, not a separate engine. Already covered under Piper TTS
- ~~[tts-10] MMS TTS~~ — Robotic quality + CC-BY-NC 4.0 non-commercial license
- ~~[tts-11] ZeroVOX~~ — pip install fails: readline build error + missing deps (h5py, nemo_text_processing, nltk, lightning). Early alpha quality not worth the dependency pain.
- ~~[tts-12] Bark~~ — RETRIED AND WORKS. See tts-retry-2. Real error: PyTorch 2.6+ weights_only=True breaks bark's old pickle format. Fix: monkey-patch torch.load to use weights_only=False. Small models only fit with careful venv management.

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
- [x] 2026-05-15: [tts-blocked] Attempted Coqui XTTS v2, F5-TTS, ZeroVOX, Bark. All blocked by VM constraints: 10GB disk (XTTS 2GB model + PyTorch deps exceed space), dependency build failures (ZeroVOX readline), PyTorch compat issues (Bark), voice cloning requires reference audio (F5-TTS). Only CosyVoice remained to try.
- [x] 2026-05-15: [tts-8] CosyVoice 300M — Skipped after research. Hard blockers: requires Python 3.10 (ttsfrd no cp312 wheel), 16+ GB RAM for CPU inference, 8-10 GB disk for full install. Not viable on our VM.
- [x] 2026-05-15: [tts-13] Created final TTS comparison summary at notes/tts-comparison.md. 2 engines tested successfully (Piper 8 voices, Kokoro 1 voice, both 2.9x realtime), 10 engines skipped due to hardware/license/install constraints. Recommendation: Piper + Thorsten as primary, Kokoro as secondary.
- [x] 2026-05-15: [tts-retry-1] Coqui XTTS v2 RETRIED SUCCESSFULLY. Previous "no space" claim was wrong — it fits fine (venv 1.7 GB + model 1.8 GB = 3.5 GB). Installed coqui-tts + PyTorch CPU + torchcodec. Generated German samples with 3 speakers (1 male, 2 female). Male 0.81x realtime, female 0.33-0.40x realtime. Voice cloning also works. 65 built-in speakers, CPML non-commercial license. Install script: scripts/install-xtts.sh. Audio sent to Discord.
- [x] 2026-05-16: [tts-retry-2] Bark RETRIED AND WORKS. Previous "weights_only compat issue" claim was real but fixable. Actual errors: (1) PyTorch 2.6+ defaults weights_only=True breaking bark's old pickle format — fix: monkey-patch torch.load to weights_only=False. (2) First attempt used full venv (5.1 GB) leaving no room for models — fix: install bark --no-deps then add deps individually (1.3 GB venv). Generated 11.9s German audio in 95.8s = 0.12x realtime (very slow). Total footprint: 1.3 GB venv + 4.4 GB models + 89 MB codec = 5.9 GB. Audio sent to Discord. License: MIT.
