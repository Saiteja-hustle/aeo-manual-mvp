# 00. Master SOP: the AI visibility loop

## PART A. HUMAN OVERVIEW

### What this is
A manual process that answers one question for a client: if we make honest changes to their pages and presence, does Google's AI Overview start naming their product? It is a Manual MVP. The goal is to learn what to automate, and the output is a plan plus a tracker, not finished articles.

### The loop (what I did, in order)
1. **Keywords.** Pull queries the site already ranks for in Google Search Console (GSC). Pick a small set. (SOP 01)
2. **AI Overview check.** Search each in incognito. Does an AI Overview show? Is the product named? Cited? Log it with a fixed capture format. (SOP 01)
3. **Reasons.** If we show up, why? If not, why not? (SOP 02)
4. **Citation analysis.** For each tool in the answer, find the source behind it and classify it. Compare cited pages with our pages. Write the audit doc. (SOP 02)
5. **Opportunities.** Turn patterns into articles (on-page fixes), discussions, and listings or mentions. Each with a why, a how, evidence, and an AI prompt. (SOP 03)
6. **Tracker.** Put it all in a Notion page the client can read: observe, understand, execute. (SOP 04)
7. **Re-check loop.** Ship one fix per day, log the date, re-run the prompts at day 3, day 7, day 14 and the final check. Update the tracker. (This file, below)

### Worked example (CursorClip, Oct 2026)
- 25 prompts planned, cut to 6 on 11 Oct (manual tracking took too long, before any fix shipped), then to 4 tracked: screen studio alternative, best screen recorder for mac, loom cheaper alternative, tella alternative.
- Baseline 11 to 13 Oct. Result: product named in 0 of 4 answers, despite ranking on Google for all four.
- Biggest findings: the AI lifts descriptions from each tool's own page or third parties; four doors into answers (vendor page, directory, YouTube, forum thread); one source can feed several lines; conflicting facts across the web.
- No fix shipped at baseline, so no lift was claimed.

### Timeline template
| When | Check |
|---|---|
| Day 1 to 3 | Baseline runs (3 per prompt, 2 devices if possible) |
| Day 3 | Sanity re-check. Too early for lift. |
| After first fix ships | Day 7 and day 14: 3 runs each |
| Around day 21 | Final check and the pay-to-continue decision |

### How to word the verdict (do not overclaim)
"Baseline measured. Fixes planned. Lift and willingness to pay tested around [final check date]. Continue, narrowed." Keep two questions separate: (a) can we improve visibility, (b) will founders pay for it. Validate (b) with the Mom Test. Question 5: "Tell me about the last time a third-party page described your product incorrectly. What did you do?"

### Daily routine (15 to 30 minutes)
1. Run today's re-checks using the capture sheet (SOP 01).
2. Paste the runs plus the daily refresh prompt into Claude (`prompts/daily-refresh.md`).
3. Spot-check every changed row. Do not trust unverified lines.
4. Ship at most one fix. Log the date, URL and GSC position before.
5. Note any scope change in the scope log.

## PART B. AI AGENT INSTRUCTIONS

**Role:** operations assistant for an AEO manual MVP. You follow the SOPs in this pack in order and never skip the capture format.

**Inputs you need before starting:** client site URL, GSC export (queries and pages, last 3 months), list of competitors known to the client, the tracker URL (if it exists), and the scope log.

**Procedure:**
1. If no keyword set exists, run SOP 01.
2. If captures exist but no analysis, run SOP 02.
3. If analysis exists but no plan, run SOP 03.
4. If a plan exists but no tracker, run SOP 04 (build). If a tracker exists, run SOP 04 (refresh).
5. After any change, update the scope log and the "last checked" dates.

**Rules:**
- Mark every unverified number `[VERIFY]`. Never invent prices, sizes, dates, or quotes.
- Use "observed" for what we saw. Use "tested" only for controlled checks.
- Never write personal names, emails or contacts into the tracker.
- Never propose fake independent sites, fake reviews or undisclosed promotion.
- Keep product work (adding features) out of the plan. Note it as "product roadmap".

**Done when:** every prompt has a baseline, an audit doc, plan rows with side pages, and a tracker that matches the audit docs.
