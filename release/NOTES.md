## KWS 1.2.6.0 — StreamRecorder joins KWS

### Connected services
Settings now has **Connected services** instead of log-source options. Connect an account and KWS uses it automatically, each with a status light (🟢 Pro/Premium · 🟡 free · 🔴 logged out) and a ↻ check:
- **StreamRecorder** (Twitch · Kick · SOOP · CHZZK recordings)
- **KickLogz** (Kick chat logs) — the Free/Pro choice now follows your account by itself

### StreamRecorder
- Hits KWS can't play — VOD deleted, sub-only, no VOD time, or Twitch VODs blocked in your region (e.g. Korea, option "Always open Twitch hits in the recording") — open the **recording of that broadcast**, 30 s before the moment.
- They play in a small **KWS player window** (same look as the inline players: quality, 1–4x, ±10 s double-click, hold for 4x) that is **reused** for the next hit; same recording → it just jumps.
- **Clip download** from the recording (start/end, quality) — saved as one .mp4 that starts at 0.
- **Twitch dual source:** with StreamRecorder on, Twitch scans also search StreamRecorder's recorded chat next to Zonian (fills gaps when Zonian is rate-limited).
- Streamer not on your StreamRecorder list → KWS adds it (Premium sees older recordings right away); list full → KWS removes the streamer you searched least recently.
- SOOP sub-only VOD screen gets a "Watch the StreamRecorder recording" button.

### Fixes & more
- Twitch: Zonian rate limiting (429) handled — waits and retries instead of failing dozens of days; the message now says when Zonian is limiting.
- Results tell you what Pro/Premium would have added (with the real count).
- Tab menu: "Remove from history + close tab".
- Since 1.2.5.54: Paper / Midnight themes with preview cards, "Find new streamers" card, GitHub update notice.
