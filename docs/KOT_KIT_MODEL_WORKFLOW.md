# Kot Kit — Live2D model workflow

> Planning document. This workflow has not yet been validated end to end.

## Scope

Three original characters: Yellow Cat (`yellow-cat`), Masik (`masik`) and Busik (`busik`). Masik and Busik will be designed from photographs supplied later. Do not assign a breed to Masik based on appearance alone. Keep a shared visual style, with distinct character features.

## Minimal pipeline

1. Prepare the character artwork and separated layers, including hidden areas needed for motion.
2. Export a layered PSD and a concise per-layer/parameter rigging guide.
3. On a separate computer with Live2D Cubism 5.3, import the PSD, create/adjust ArtMeshes, deformers and parameter keyforms, and save the editable `.cmo3` project.
4. Export the native `.moc3`, textures and `.model3.json` from Cubism. A PSD or a set of JSON files is not a substitute for a compiled `.moc3`.
5. Prepare compatible motion/expression JSON and test the model in a local preview before integrating it with DSH.
6. Verify agent-state reactions, click interactions and character switching in `dsh-live2d-kot-kit`.

## Suggested shared parameter IDs

Start with `ParamEyeLOpen`, `ParamEyeROpen`, `ParamMouthOpenY`, `ParamAngleX`, `ParamAngleY`, `ParamAngleZ`, and custom parameters for ear and tail movement. These are proposed conventions, not a verified rig or a guarantee that motion files are interchangeable across characters.

## Order of work

- **Yellow Cat:** minimal proof of concept (blink + mouth + tail), validate Cubism export and DSH integration.
- **Masik:** create artwork from the real cat's photographs and adapt the proven rig.
- **Busik:** repeat with the other cat's individual features.

## Release boundary

Before the first public release, remove original Whale Girl artwork from release packages, check remaining embedded assets and their licenses, verify model rights, and replace upstream-only instructions and screenshots. Preserve required code attribution and notices.

## Working rules

Keep the project lightweight: no remote worker, GUI orchestration service, or automatic Cubism compiler. The human follows explicit editor steps; Codex handles preparatory assets, documentation, configuration and integration code.
