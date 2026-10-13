# 03. Opportunity plan (step 5)

## PART A. HUMAN OVERVIEW

### What I did
From the patterns, I listed concrete opportunities in three tracks. Each is a row with a why, a how, the evidence, and an AI prompt Claude can run. The output is a plan, not finished article drafts.

### Track A: Articles (on-page fixes)
Types: FAQ, Quick-answer block, Honest section, Freshness line, New page, Page rewrite, Entity and schema, Small edit. Each row has Prompt, Type, Target URL, Why, Priority (1 to 4), Effort (S/M/L), Status, Ship date. Examples we planned:
- Rewrite the homepage opening with a plain "best for" sentence and feature list.
- Build an exact-match page named for the query.
- Restructure the pricing-guide page so its title and first answer match the query.
- New list pages ("Cheaper Loom Alternatives for Mac", "Tella Alternatives for Mac").
- Make price, size and free-vs-paid facts match everywhere.
- Add FAQ, honest "when X is better" section, "checked on" date.
- Entity and schema (About page, Organization and SoftwareApplication schema).

### Track B: Discussions
Reddit, Hacker News, YouTube. Rules: one real account, founder disclosed, answer the question asked, no pitch, 2 to 3 genuine replies a week. Check the thread is open first. Skip closed or old threads. Own maker post is phase 2 (day 15 or later). YouTube: ask creators to include the product, offer a free licence, creator must disclose.

### Track C: Listings and mentions
Websites only (not names or contacts): directories, community lists, blogs and roundups, editorial, fact fixes on existing profiles, our own channel. Fields: website, link, prompt, type, what it feeds, action, cost, status.

### Prioritising
Fastest and widest first: make facts match everywhere (helps every prompt), then homepage opening, then exact-match pages, then listings that feed several lines (a directory behind 3 of 4 lines), then slow outreach. Ship one fix per day and log the date so any change in the answer can be tied to one fix.

### Not doing
- A second domain that writes "alternatives" articles and promotes the product as if independent. It is undisclosed promotion and it would break the test. A clearly branded own blog or channel is the legitimate version.
- Feature work (captions, share links). Note it for the product roadmap.

## PART B. AI AGENT INSTRUCTIONS

**Role:** AEO planner. You turn audit findings into plan rows.

**Inputs:** audit docs (SOP 02), tracker schema (SOP 04), verified facts list from the client.

**Procedure:**
1. For each pattern in the audit, ask: is there an on-page fix, a discussion, or a listing that addresses it?
2. Create one row per action. Title is a short imperative. Fill Prompt, Type, Target URL, Why (one sentence), Priority, Effort.
3. Priority rule: 1 = fixes that help every prompt or copy a proven pattern; 2 = prompt-specific, cheap; 3 = depends on a result or is slow; 4 = optional.
4. Effort rule: S under a day, M 2 to 3 days, L more than 3 days.
5. For every row write a side page using `templates/side-page-template.md`: Why we are doing this; How to do it (numbered steps); Evidence (cite the audit: what Cap, Screenhance, Tool Finder or others do); What to check afterwards; AI prompt for Claude (code block).
6. In every AI prompt: state the product facts to use; instruct `[VERIFY]` for anything missing; require disclosure ("we make X"); forbid copying other sites' wording; forbid invented numbers; ask for 2 variants for outreach.
7. For discussions, the prompt drafts the comment or an overview of it. For listings, the prompt writes the submission or outreach for the website, with no names or contacts.
8. Mark closed or low-fit threads as `Skip` and give the reason on the page.
9. Order a one-fix-per-day schedule.

**Rules:**
- No personal names, no emails, no contact details.
- Do not hide product limits. Pair each "lacks" line with "when it wins".
- Anything the AI showed as a price is `[VERIFY]` until checked on the vendor's page.

**Done when:** every row has a side page with an AI prompt, no row has an unexplained one-liner, and a ship order exists.
