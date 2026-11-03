## KWS 1.2.6.10 — hotfix

Install over 1.2.6.9 (everything in 1.2.6.9 still applies).

- **SOOP inline player**: it could stop by itself 1–2 s after pressing play, start silent, or not start at all when the SOOP tab had been used for a search. KWS's "keep the search tab quiet" step paused every video in that tab every 3 s — including the KWS player. It now only touches the site's own videos (YouTube search tabs fixed the same way).
- **SOOP inline player**: when Chrome won't autoplay with sound (opened from the side panel), it starts muted with a "🔇 Tap for sound" button instead of not playing.
- **SOOP → StreamRecorder** opened a different broadcast's recording. KWS now keeps each SOOP VOD's time and length and opens the recording of that same broadcast, at the matching moment. Results searched before this version use the old guess — search the channel again once.
