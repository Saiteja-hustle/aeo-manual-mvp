# 01. Keywords and AI Overview check (steps 1 and 2)

## PART A. HUMAN OVERVIEW

### What I did
**Step 1. Keyword research.** I looked in Google Search Console for queries the site already ranks for, over the last 3 months, with impressions, clicks and average position. I wanted queries that already get impressions, because it is easier to be named for something Google already trusts us on. I grouped near-duplicate variants that return the same AI answer (for "best screen recorder for mac" there were five variants adding up to about 6,700 impressions).

**Step 2. AI Overview analysis.** For each chosen query I searched in incognito Chrome (Hyderabad, MacBook, plus some mobile runs). I recorded: did an AI Overview show, is the product named in the answer text, is it cited in the sources, which tools are listed, the group headings, and each tool's source badge.

### The four prompts we tracked (CursorClip)
| # | Prompt | Position | Impressions (3 mo) | Clicks |
|---|---|---|---|---|
| 1 | screen studio alternative | 2.3 | 2,251 | 346 |
| 2 | best screen recorder for mac | 7.6 | 1,752 | 17 |
| 3 | loom cheaper alternative | 9.25 | 1,381 | 0 |
| 4 | tella alternative | 8.35 (page) | 1,366 | 2 |

Notes: for #2 the ranking page (a roundup) averages 11.2. For #4 the numbers are for the Tella page, not the query.

### Scope decision (log it openly)
I planned 25 prompts, cut to 6 on 11 Oct because manual tracking took too long, before any fix shipped. Then cut to 4 tracked. Siddhant's feedback: lock the prompts before fixes, and log scope cuts openly.

### Gotchas I hit
- Sources change by run and device. Only compare what holds across runs.
- Source badges show only the first source. "+N" hides others, and redirect links stop you confirming the exact page.
- A tool can be named in the answer with no visible badge.
- Reddit and TechRadar sources appeared on 11 Oct and not on 12 Oct. Treat them as unstable.
- Right-hand cards (YouTube, vendor pages) are separate from in-line badges. Record both.

## PART B. AI AGENT INSTRUCTIONS

**Role:** keyword analyst and AI Overview capture assistant.

**Inputs:** GSC queries export (last 3 months: query, clicks, impressions, position), GSC pages export, the client's product name, and the capture sheet filled by the human (see `templates/capture-sheet.md`).

**Procedure (keyword selection):**
1. Read the GSC queries. Drop branded queries.
2. Group variants that likely return the same AI answer (same intent, word order changes). Sum impressions per group.
3. Rank groups by impressions, then by how winnable they are (position under 15, intent matches the product).
4. Propose 4 prompts. Prefer one for each intent type: alternative-to-X, best-for-category, cheaper-than-X, comparison.
5. Output a table: prompt, variants merged, impressions, clicks, average position, ranking page.
6. Write the proposed list in the scope log with date. After the human approves, lock it. Changes after locking must be logged with a reason.

**Procedure (AI Overview capture, human performs, AI structures):**
1. For each prompt, the human runs 3 searches under the same conditions: incognito Chrome, same city, same device. Optionally 1 run on mobile with the sources panel open.
2. For each run, fill one row of the capture sheet.
3. Compute per prompt: AIO shown (yes/no, how many runs), named (runs out of 3), cited (runs out of 3).
4. Apply the success rule: the product counts as named only if it is in the answer text in 2 of 3 runs.
5. Map the Verdict: `Not in the answer` (not named), `Partly in the answer` (cited, not named), `Named in the answer` (named in 2 of 3 runs).

**Output format:**
- A prompts table (as above) with the verdict.
- A run log table with every run.
- A "what held across runs" list: tools and sources that appeared in all runs.
- A "rotating slots" list.

**Rules:**
- Never conclude from a single run. Say "observed on [date], one run".
- Do not merge sources that differ between runs.
- If GSC shows only one variant, track that variant. Record other variants as a second check.

**Done when:** four locked prompts, a baseline of at least 2 days, and a capture log with the verdict per prompt.
