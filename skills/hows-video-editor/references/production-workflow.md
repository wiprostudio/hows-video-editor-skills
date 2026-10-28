# HOW's production workflow

## Reference and evidence limits
Adapted from the owner-supplied BeyondStudio tutorial MP4 (152.469 seconds), reviewed through 16 sampled frames. Visual review only: no audio transcription or continuous playback was performed. Approximate source positions:
- 28–57s: project rules and separate STYLE.md.
- 66s: script before production.
- 76s: timed treatment/storyboard.
- 85s: frame = f(t).
- 95s: continuous voice recording.
- 114s: feedback naming a specific scene and visible defect.
These are sampling positions, not exact segment boundaries. The tutorial's branch, commit, resolution, logo and no-render rules are examples from its project, not instructions for this repository.

## Apply to HOW's
1. Brief: topic, audience, format, desired runtime, production route, deliverable and budget if paid services are requested.
2. Research: use us-story-research when available; otherwise collect sources and map material claims. Draft in Indonesian for owner review.
3. Prose pass: use humanizer when available to remove filler while preserving facts, citations, uncertainty and deliberate narrative rhythm. Never add an event, visual clue or quote to make factual narration more vivid.
4. Script review: prepare the requested review artifact. Produce full American English adaptation after approval or explicit bilingual/English authorization.
5. Treatment: use templates/TREATMENT.md and STYLE.md. Draft estimated scene timing before coding; reconcile with measured final narration later.
6. Visual pilot: implement a representative 10–20-second section before extending a new visual system to an entire episode. This is a production check, not a repeated permission gate.
7. Animation: each rendered frame depends on frame/time, fixed configuration and assets. Remotion: useCurrentFrame plus fps. Canvas/SVG: expose a seek/render-at-time function. Avoid wall-clock timers and unseeded randomness in exported animation; wait for fonts/assets to load. For identical render conditions, seeking directly to a frame must match reaching it by playback.
8. Voice: for a short episode prefer a continuous take to preserve cadence; long episodes may use sections or pickups. TTS is optional. Measure audio, align scene boundaries and preserve natural pauses.
9. QA: inspect scene entry, middle, exit and transitions; check clipping, overlap, layering, map/chart accuracy, caption safe areas and sync. Play the full final export and listen before claiming complete audiovisual QA.
10. Revision: identify scene ID, timestamp/frame, observed defect and expected result. Patch the affected component and inspect its neighboring transitions.
11. Deliver: editable source, MP4 when requested, source/asset provenance, and truthful validation notes.

## Requirements and status
Confirmed in this workspace: Node v24.22.0, npm 11.19.1, Git, installed Humanizer, available us-story-research, experimental HOW's editor skill and local prompt library.
Not prepared yet: Remotion project, locked dependencies, scene components, working render command and export QA. Standalone ffmpeg/ffprobe were not found on PATH; check the chosen renderer's bundled encoder before installing another.
Needed for first real episode: selected topic, approved script, style assets/fonts/logo, final narration or authorized voice-generation route, desired format and runtime.
Optional: Higgsfield for generated shots, ElevenLabs or another TTS, stock library, external editor for finishing. They are not all mandatory.
No renderer or paid generation has been installed or run by this workflow adaptation.

Official implementation references:
- https://www.remotion.dev/docs/idea
- https://www.remotion.dev/docs/use-current-frame
- https://www.remotion.dev/docs/render
