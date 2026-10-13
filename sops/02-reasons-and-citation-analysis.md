# 02. Reasons and citation analysis (steps 3 and 4)

## PART A. HUMAN OVERVIEW

### What I did
**Step 3. Identify the reasons.** If the product is named, why? If not, why not? I wrote a hypothesis for each prompt, and kept it as a hypothesis until a fix was tested.

**Step 4. Citation analysis.** I reverse-engineered where each tool in the answer comes from. For every tool I noted the source behind it, classified it, and checked whether it was the same on every day. Then I opened the cited pages and our own pages side by side and compared them.

### The four doors into an AI answer
1. **Vendor page.** The tool's own page (Cap, Screen Studio, Dadan, Screenhance).
2. **Directory.** Tool Finder, Techjockey, Uneed.
3. **YouTube.** Often one video feeds several lines (one ClickUp video fed three tools).
4. **Forum thread.** Reddit, Hacker News, community forums.
Also: blogs and roundups, and editorial pages (TechRadar).

### What I compared on pages
Title and H1, shape (sections), word count, whether there is a table, FAQ (visible answers?), "when X is better" section, date or "checked on" line, price line, whether the page is named for the query.

### Patterns that mattered (CursorClip)
- Ranking is not being named. We ranked on all four and were named in none.
- The AI lifts plain claims from a tool's own page and paraphrases them into "Best for" lines.
- The cited page can be small (Cap's is about 320 words).
- Independent sources can be old or thin. Freshness and size do not decide who gets cited.
- The AI groups tools by pricing model; the one-time group was thin.
- Conflicting facts across the web (price and size) are a risk.
- A tool's own channel or page gets it listed.

### A third-party analysis came in. How I handled it
Treat it as data, not truth. List each claim, mark `Not verified` or `Matches what I found`, and say where I agree and where I push back. Example: it said roundups feed the answer, but in our captures vendor pages and YouTube did, so we started with what we saw cited.

### Audit doc structure (one per keyword)
Summary; 1 Keyword analysis; 2 Diagnosis (tool, source, type, same across days?); 3 Patterns; 4 Action plan (Track A on-page, Track B discussions and outreach, Track C listings); 5 How we measure; 6 Open items. Use `templates/audit-doc-skeleton.md`.

## PART B. AI AGENT INSTRUCTIONS

**Role:** citation analyst. You work only from the capture log and pages the human supplies.

**Inputs:** capture log (SOP 01), screenshots or notes of source badges, text of cited pages, text of our matching pages, GSC data, any third-party analysis.

**Procedure:**
1. Build the diagnosis table: tool, source (domain and page), source type (vendor page, directory, YouTube, forum, blog or roundup, editorial), run dates seen, same across runs (yes, no, mostly).
2. Mark each source `stable` (in every run) or `rotating`.
3. Count: how many sources per type; which single source feeds several lines.
4. For each cited vendor page and our matching page, fill the page comparison: title/H1, shape, word count, table, FAQ, honest section, date line, price line, named for the query.
5. Write 4 to 7 patterns. Each pattern must cite evidence from the log. Label each: `observed once`, `observed across runs`, or `hypothesis`.
6. Write one hypothesis per prompt: why the product is missing, in one sentence.
7. If a third-party analysis is supplied, make a table: finding, status (`Matches what I found`, `Not verified`, `Contradicted`), and your note. Push back where captures disagree.
8. Correct our own earlier notes if a capture shows an error, and say so in a "Corrections" line.
9. Produce the audit doc using the skeleton.

**Rules:**
- Never infer a source from a single "+N" badge. Say "first source only".
- Do not treat an AI-shown price as verified.
- Do not recommend feature work as an AEO fix. Put it under "Not in this plan".
- Do not recommend fake independent sites.

**Output:** audit doc per prompt, plus a cross-prompt table (tool vs prompts it appears in) for the Overview.

**Done when:** every prompt has an audit doc with diagnosis table, patterns with evidence labels, and open items.
