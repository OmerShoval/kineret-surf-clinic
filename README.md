# Omer Shoval Surf Clinic — Website

Production-ready single-file site for the July 2026 wakesurf clinic on the Sea of Galilee.
Hebrew (RTL) by default with an English toggle. No build step, no dependencies.

## Files

- `index.html` — the entire site. Tested and verified (DOM tests: dates, WhatsApp links, language toggle, sold-out states, Instagram embeds).
- `ANTIGRAVITY-PROMPT.md` — paste its contents into Antigravity (Claude Code) to verify and deploy.

## How Omer edits the site (no code knowledge needed)

Open `index.html`, find the CONFIG block at the top of the `<script>` tag near the bottom:

**Mark a paid signup** — change `taken: 0` for that date. Example, 2 paid for July 19:

```js
{ id: "19-07", day: 19, dow_he: "יום ראשון", dow_en: "Sunday",  taken: 2 },
```

The spots bar, "X spots left" label, and sold-out state (at 5) update automatically.

**Swap a video** — replace any Instagram URL in `HERO_REEL` or `STUDENT_VIDEOS`.

**Change WhatsApp** — `WHATSAPP` (number for date bookings, prefilled messages) and `WHATSAPP_LINK` (branded link for the floating button).

## Important

- Instagram embeds only render over HTTP(S) — they will NOT show when opening the file by double-click (`file://`). Preview with `npx serve` or just deploy.
- After every edit, re-upload/redeploy the file. That's the whole release process.

## Key facts baked into the site

- Dates: July 19 (Sun), 21 (Tue), 27 (Mon), 2026 · 08:00–12:30
- Price: ₪1,650 per surfer · max 5 spots per date
- Location: Migdal Boats Beach, Sea of Galilee · Nautique G23
- Booking: WhatsApp 972542491388 · branded link wa.me/message/COL2U5IJP56IB1
