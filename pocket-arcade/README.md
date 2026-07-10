# Pocket Arcade

A clickable prototype of an all-in-one revival of the golden-age one-tap iPhone games —
six playable games, XP progression, leaderboards, phone sign-in with SMS opt-in, and a
one-time "Arcade Pass" purchase flow.

Everything lives in a single dependency-free file. Open `index.html` in any browser
(best on a phone or a narrow window).

## The games

| Game | Inspired by | Status |
|---|---|---|
| Wing It | Flappy Bird | free |
| Pulse Runner | Geometry Dash | free |
| Sky Hop | Doodle Jump | free |
| Spin Tap | Pop the Lock (original twist) | free |
| Lane Dash | Subway Surfers / Temple Run | Arcade Pass |
| Stack Drop | Stack (original twist) | Arcade Pass |

All names, art, and code are original. Mechanics aren't copyrightable, but the classic
games' names, characters, and art are trademarked/copyrighted — don't ship with them.

## What's real vs. simulated in this build

**Real:** all six games, scoring, XP/levels, coins, per-game best scores, the free/locked
split, sound effects (WebAudio), haptics, persistence via `localStorage`.

**Simulated (needs a backend to ship):**
- **Leaderboards** — currently seeded local bots plus your best score. Ship with a small
  API (Supabase/Firebase) or Game Center / Google Play Games.
- **Phone sign-in** — the form collects name + phone + a separate marketing-consent
  checkbox, but sends no SMS and stores nothing off-device. Ship with Firebase Phone Auth
  or Twilio Verify for the OTP, and keep marketing consent as its own recorded opt-in
  (TCPA requirement — verification consent is *not* marketing consent).
- **Arcade Pass** — the buy button flips a local flag. Ship with StoreKit / Google Play
  Billing and verify receipts server-side.

## Monetization note

The $2.99 price is wired up as a **free download + one-time unlock IAP** rather than a
paid app listing. Paid listings convert far worse than free-with-unlock, and this way
players try four games before being asked to pay.
