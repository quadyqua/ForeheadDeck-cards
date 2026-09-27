# Forehead Deck: cards

The live card list for the Forehead Deck iPhone app. The app downloads `cards.json` from this repo on launch, so changes here reach players without an App Store update.

## Monthly update
1. Edit `cards.json`: add new cards, and retire stale ones.
2. Bump `"version"` to something that sorts **later** (e.g. `"2026-10"`). The app only swaps in the new list when the version is newer than what it has.
3. Merge to `main`. Players get it the next time they open the app.

Each card looks like this:

```json
{"id": "stars:Lamar Jackson", "name": "Lamar Jackson", "hint": "Ravens QB", "cat": "stars",
 "emoji": "🐦‍⬛🏈⚡️", "actor": false, "online": false, "adult": false}
```

- `cat` is one of `stars`, `toons`, `memes`, `classics` or `kids`, and `id` is `cat:name`.
- `actor: true` hides the card when "Leave out actors" is on.
- `online: true` hides it when memes are off.
- `adult: true` hides it in kid-safe mode (horror, explicit lyrics, adult cartoons).

**Rules for new cards:** text only (no image links, no code). No mean-spirited or sexual hints about real people. Skip anyone recently in the news for a death or scandal.

## Pages
- `privacy.md`: the app's privacy policy (linked in the app and in App Store Connect)
- `index.md`: support page
- `deck.html`: where shared custom-deck links land. It reads the deck from the link and offers "Open in Forehead Deck."

