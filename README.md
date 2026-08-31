## Index

| Day | App | Stack Type | Live Link | Notes |
|-----|-----|-----------|-----------|-------|
| 001 | Fillup | CRUD (touched API integration too) | [ https://stupendous-axolotl-5b0503.netlify.app/ ] | food/calorie tracker, scope grew a lot |

*(newest entries added to top of table as the log grows)*

---

## Entries

### Day 001 — Fillup
**Date:** Aug 31, 2026
**Stack type:** CRUD, vanilla HTML/CSS/JS (ended up touching API integration too)
**Live:** [https://stupendous-axolotl-5b0503.netlify.app/]

**Scope:** A calorie and protein tracker. Set a daily goal, log food, watch two tanks fill up as you go. Started as a simple manual-entry tracker and grew into food search (built-in food list, sized drinks, common restaurant chain items), a personal "saved foods" memory system, and a full cozy pixel-game visual redesign.

**The bug:** Built food search on a live Open Food Facts API call first. Mid-build, discovered the legacy search endpoint was down site-wide — a real outage, not a local bug. Pivoted to a bundled local food list instead, which turned out to be more reliable for a daily-use tool anyway (no network dependency, can't go down).

**What I learned:** Scope creeps hardest right after something starts working — each new feature (chain restaurant data, save-your-own-food memory, visual reskin) felt like a small add in the moment, but stacked up to a much bigger Day 1 than planned. Worth noticing when to keep saying yes vs. cut and ship. Also: don't build on an external API without a fallback plan, even for a "just search some data" feature — pivoted to a local dataset mid-build because the endpoint was down globally. (Used Open Food Facts API)

---



