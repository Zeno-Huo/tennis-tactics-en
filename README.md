# Tennis Tactics — All-English 2K Animations

Two all-English, 2K animated breakdowns of tennis tactics — six winning singles plays and six classic doubles team plays — built with Grok, Three.js + HTML, then rendered to video with sound.

## Videos

| Video | Resolution | FPS | Duration | What it covers |
|---|---|---|---|---|
| [`Tennis_Singles_EN_2K_with_audio.mp4`](Tennis_Singles_EN_2K_with_audio.mp4) | 1440 x 2560 | 24 | 75 s | 6 winning singles tactics: cross-court to line, deep ball + drop shot, wide serve attack, inside-out forehand, deep ball + follow to net, overhead lob |
| [`Tennis_Doubles_EN_2K_final.mp4`](Tennis_Doubles_EN_2K_final.mp4) | 1440 x 2560 | 24 | 75 s | 6 classic doubles plays: server poach, pin the feet + force a lob, deep return + partner poach, squeeze the middle, serve and volley + twin net rush, lob to force a switch |

Both videos carry the original Web Audio track — background music plus ball-hit and bounce effects, with fade in/out, ducking under contact, and stereo panning.

## Source HTML

The editable all-English sources are included:

- `Tennis_Singles_6_Plays_EN.html`
- `Tennis_Doubles_6_Plays_EN.html`

Open either file in a modern browser. It renders a Three.js 3D court; use the built-in controls to play, pause, seek, change speed, and toggle sound. The animation is 1080 x 1920 at its native resolution and exposes `window.render(t)` for frame-accurate seeking.

## How they were made

1. **Tactic design** — Grok was used to draft the tennis tactics and their shot-by-shot sequences.
2. **3D animation** — the plays were built as self-contained HTML files with Three.js, with the court, players, ball trajectories, captions, coach annotations, and a Web Audio soundtrack (music + effects scheduled to each contact).
3. **English version** — all Chinese UI, captions, tactic data, and coach labels were translated to English, including the logic that keys off tactic titles.
4. **2K video** — each frame was rendered via `window.render(t)` and captured, then assembled into 1440 x 2560 H.264 video at 24 fps.
5. **Audio** — the Web Audio track was rendered offline (OfflineAudioContext) using the page's exact event schedule and mixed into the final video as AAC stereo.

## License

Released into the public domain (CC0). Feel free to use, remix, and share.
