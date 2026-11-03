## KWS 1.2.6.9 — calmer home, ★ daily check, friendlier StreamRecorder

### New in 1.2.6.9
**Home**
- Calmer home: channels you haven't checked in a while come first; one tools card for **Find streamers**, **★ check favourites daily** and **🌙 overnight mode** (moved here from Settings); tips fold into one line.
- **★ Check favourites daily**: once a day KWS scans your ★ channels for new VODs by itself; new hits show as a number on the toolbar icon and a "show" button. "Check now" runs it right away.
- First run shows a 3-step "Getting started" card; old-history import moved under it.
- Press the open platform tab again → its home (cards), with your ID tabs kept on top.
- Right-click "search all" / 🎲 → search more at once: the 8 / 15 / 30 longest unseen, every channel with a memo, every ★ favourite, everything not checked lately.
- Find streamers opens a chooser: StreamRecorder latest list, TwitchTracker ranking, KickLogz keyword search, SOOP ranking. The KWS site badges there are always on.
- Wider panel → short names next to the platform dots; narrow → just the dots.
- Input hints per platform, and pasted Twitch / Kick / SOOP channel addresses work.
- New installs close 0-hit tabs automatically.

**Results**
- Zonian + StreamRecorder (and Zonian + Native API) no longer show the same chat line twice (login vs display name); merged lines keep the VOD time or the recording moment.
- StreamRecorder hits look different: teal with an **SR** tag, time = the moment in the recording. A hit with no VOD time that you open in StreamRecorder once keeps that recording time from then on. SR hits translate too.
- No-VOD hits: the button says ⚠ VOD expired (real time only in the tooltip); inside a run they show **+5s**, **+1:10** after the run's first hit.
- Purple (playable) times open the inline player straight away; the Try native / StreamRecorder menu is only for ⚠ hits (right-click still lets you choose).
- Keyboard: ↑↓ move between hits, Enter plays, Space marks seen.
- Twitch: days Zonian refused mid-scan say "fetched again at the end (automatic)" instead of "couldn't fetch".
- Closing a result tab moves to the tab next to it; tab menu close items reordered (this tab · others · tab + history).
- Display names shown when known (login in the tooltip). Activity bar: Native API · Zonian · StreamRecorder.

**Downloads**
- Clip Downloader in your language on every player (Twitch, Kick, SOOP, CHZZK, StreamRecorder).
- StreamRecorder: each download gets its own progress window (several at once), the clip range shows on the seek bar, file names like `00h30m00s-00h45m00s-<id>-<date>-1080p.mp4`, sound and picture start in step (no stutter at the start), and the window won't close while downloading.
- End past the VOD's end → set to the VOD's end (name and length match).

**StreamRecorder player**
- Speed / volume centred like the other players; plain-words errors (still recording / not found / login).

**Also**
- Site badge clicks give instant feedback on a slow computer ("starting…", "busy — no need to click again", "click once more to open the panel").

---

## Earlier (since 1.2.6.0)

### 1.2.6.8
- **Settings: basic / advanced.** Keywords, theme, quality and Connected services up front; badges, SOOP mode, results, overnight mode and data backup fold under **Advanced settings**.
- **Zonian status light** in Connected services (🟢 working · 🟡 resting after too many requests, with a countdown · 🔴 not answering). During a Twitch scan the progress line says in plain words when Zonian is resting and when it continues.
- **Site badges as cards:** switches for the KWS badges on streamrecorder.io lists and on twitchtracker.com.
- **Plain-words errors** (busy server, connection, timeout, login) instead of raw codes — the technical text stays in brackets.
- **Time left** on running scans ("about 3 min left").
- **Export results** from the tab menu: copy as text (time · name · chat · link) or save as CSV for Excel / Google Sheets.
- **Hits whose VOD is gone keep their time** (⚠ 01:23:45 in the error colour); the reason is in the tooltip.
- **Clip downloads always start on the best quality** (Source / original), not whatever is playing — SOOP, Twitch, Kick, StreamRecorder.
- **StreamRecorder player:** a small "HLGX · Keyword Searcher" loading screen with a live terminal-style log of each step; an already-open player window now comes to the front (or flashes in the taskbar).
- **Kick:** "Checking your KickLogz login…" while a search waits on it; "Find streamers by keyword" locks its button and shows each stage (login check → preparing → searching N/M).
- KWS explains why before Chrome asks for the kicklogz.com / CHZZK permission.
- Update notice shows the 3 install steps when you download.
- Activity bar: "StreamRecorder" → "SR API".
- Cleanup: removed leftover DeepL / OpenAI permissions (translation is Google only) and dead settings code.

---

## Since 1.2.6.0

### Connected services
Settings now has **Connected services** instead of log-source options. Connect an account and KWS uses it by itself — each with a status light (🟢 Pro / Premium · 🟡 free · 🔴 logged out), a ↻ check and an on/off switch:
- **StreamRecorder** — recordings of Twitch, Kick, SOOP and CHZZK broadcasts
- **KickLogz** — Kick chat logs (Free / Pro now follows your account automatically)

Each row says what Pro / Premium adds, and scan results tell you what you missed without it (with the real number).

### Watch what KWS couldn't play
- KWS judges each hit: ones it can't play inline — sub-only / expired Kick VODs, hits found only in StreamRecorder chat — open the **StreamRecorder recording of that moment** right away, 30 s before the chat line.
- Twitch hits that likely won't play (no VOD time, or Twitch hiding VODs from your IP, e.g. Korea) ask **Try native / StreamRecorder** at once — no waiting for the player to fail. With a VPN, VODs show again and they open in the inline player as usual.
- **Right-click a hit's time** to pick by hand: KWS inline player or StreamRecorder recording.
- Recordings play in a small **KWS player window** with the same look as the inline players (quality, 1–4x, double-click ±10 s, hold for 4x). It opens with a KWS loading screen, is reused for the next hit, and just jumps when it's the same recording.
- **Clip Downloader** — the same popup as the other players; asks where to save, names files like `<streamer> <d Mon yyyy>.mp4`, and the clip starts at 0.
- Streamer not on your StreamRecorder list → KWS adds it (Premium sees older recordings right away); list full → KWS removes the streamer you searched least recently. Streamers StreamRecorder never recorded aren't added.

### Twitch: two log sources
- With StreamRecorder on, Twitch scans also search StreamRecorder's recorded chat next to Zonian (shown in the activity bar).
- Zonian rate limiting (429) handled: KWS waits and retries instead of failing dozens of days, and says so when Zonian is limiting.

### Also
- Tab menu: "Remove from history + close tab".
- Since 1.2.5.54: Paper / Midnight themes with preview cards, "Find new streamers" card and history link, update notice from GitHub.
