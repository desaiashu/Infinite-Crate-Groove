# Infinite Crate Groove

A [Songbird](https://tivra.com) project.

| | |
|---|---|
| Tempo | 126 BPM |
| Meter | 4/4 |
| Tracks | 17 |
| Clips | 412 |
| Plugins | 65 |
| Automation lanes | 0 |

## Tracks

- Kick 1-Group
- Undergroove 1-Group
- Automated overgroove 4-Group
- Shakers 4-Group
- Clap 7-Group
- Clap 7-Group
- Clap 7-Group
- Audio
- 14-KORG MS-20 V 13-Group
- 15-KORG MS-20 V 13-Group
- 16-KORG MS-20 V 13-Group
- Vox
- 18-Statement Lead
- Audio
- A-Long Reverb
- B-Short Reverb
- C-Delay - Console 1

## Layout

- `bird/` — one generated `.bird` per arrangement: its sections, tracks and clips as readable notation. Rewritten on every save; edits belong in the app.
- `entities/` — content keyed by stable id (clips, plugins, automation, channels). Each file stays whole until it grows large, then transparently shards into `entities/<type>/NN.json` so merges stay size-independent.
- `spaces/` — projections that place entities (arrangement rows, mixer bus) plus per-user workspaces under `spaces/users/<id>.json` (open tabs, active tab, playback scope).
- `state/` — global project state (transport, settings, sections, …).
- `samples/` & `visuals/` — media payloads, stored in R2 (see `manifest.json`).
