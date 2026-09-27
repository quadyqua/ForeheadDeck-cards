# Forehead Deck: cards

The live card list for the Forehead Deck iPhone app. The app downloads `cards.json` from this repo on launch, so changes here reach players without an App Store update.

## Monthly update
1. Edit `cards.json`: add new cards, and retire stale ones.
2. Bump `"version"` (e.g. `"2026-10"`). The app only swaps in the new list when the version changes.
3. Merge to `main`. Players get it the next time they open the app.

Each card looks like this:

```json
{"id": "stars:Lamar Jackson", "name": "Lamar Jackson", "hint": "Ravens QB", "cat": "stars",
 "emoji": "🐦‍⬛🏈⚡️", "actor": false, "online": false}
```

- `cat` is one of `stars`, `toons`, `memes` or `classics`, and `id` is `cat:name`.
- `actor: true` hides the card when "Leave out actors" is on.
- `online: true` hides it when memes are off.

**Rules for new cards:** text only (no image links, no code). No mean-spirited or sexual hints about real people. Skip anyone recently in the news for a death or scandal.

## Pages
- `privacy.md`: the app's privacy policy (linked in the app and in App Store Connect)
- `index.md`: support page
