## Index

| Day | App | Stack Type | Live Link | Notes |
|-----|-----|-----------|-----------|-------|
| 001 | Fillup | CRUD (touched API integration too) | [ https://stupendous-axolotl-5b0503.netlify.app/ ] | food/calorie tracker, scope grew a lot |

*(newest entries added to top of table as the log grows)*

---
| 002 | Artist Quote Jar | CRUD, vanilla HTML/CSS/JS | [ADD-YOUR-NETLIFY-LINK-HERE] | quote generator, custom pixel-art jar + library background |

---

## Entries

### Day 001 — Fillup
**Date:** Aug 31, 2026
**Stack type:** CRUD, vanilla HTML/CSS/JS (ended up touching API integration too)
**Live:** [https://stupendous-axolotl-5b0503.netlify.app/]

**Scope:** A calorie and protein tracker. Set a daily goal, log food, watch two tanks fill up as you go. Started as a simple manual-entry tracker and grew into food search (built-in food list, sized drinks, common restaurant chain items), a personal "saved foods" memory system, and a full cozy pixel-game visual redesign.

**The bug:** Built food search on a live Open Food Facts API call first. Mid-build, discovered the legacy search endpoint was down site-wide — a real outage, not a local bug. Pivoted to a bundled local food list instead, which turned out to be more reliable for a daily-use tool anyway (no network dependency, can't go down).

**What I learned:** Scope creeps hardest right after something starts working. Each new feature (chain restaurant data, save-your-own-food memory, visual reskin) felt like a small add in the moment, but stacked up to a much bigger Day 1 than planned. Worth noticing when to keep saying yes vs. cut and ship. Also: don't build on an external API without a fallback plan, even for a "just search some data" feature. Pivoted to a local dataset mid-build because the endpoint was down globally. (Used Open Food Facts API)

---
### Day 002 — Artist Quote Jar
**Date:** Sept 5, 2026
**Stack type:** CRUD, vanilla HTML/CSS/JS
**Live:** [https://soft-gnome-c3f187.netlify.app]

**Scope:** A quote generator pulling exclusively from real, verified artists across disciplines — painters, fashion designers, musicians, performance and digital artists. Visual centerpiece is a pixel-art mason jar with paper "quote shreds" inside. Drawing a new quote animates a torn-paper card out below the jar, set against a custom pixel-art library bookshelf background.

**The bug:** The image for the jar was taken from a reference image of a pickle jar, and some of the old contents of the jar were still showing. Fixed by combining two masks, one that reliably catches every pixel (including dark shadow/seed specks) via flood-fill, and one that only matches genuine pickle color, so only real pickle pixels got replaced while the highlight stayed intact.

**What I learned:** I wanted to use a public API at first, but learned that no public API can filter quotes down to just artists, so I had to hand-verify a local dataset instead. Also learned that pixel art comes from drawing at a tiny resolution and scaling up with nearest-neighbor, not from vector shapes with hard corners. Smooth vector edges never read as "pixelated" no matter how blocky the corners are. (No external API used — quotes hand-verified against real interviews/sources instead.)

**Enjoyed it:** Yes


