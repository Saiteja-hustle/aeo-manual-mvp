# 04. Notion tracker: build, duplicate, refresh

## PART A. HUMAN OVERVIEW

### What it is
A client-facing Notion page that simulates the MVP. It must be easy to observe, easy to understand, easy to execute.

### Page layout (order matters)
1. Callout: what is tracked, baseline dates, headline result, success rule, how to use.
2. **Overview**: written findings (not charts), what it means, a "not proven yet" note.
3. **Prompts**: table plus a board grouped by "In the AI answer?". A legend callout explains the labels.
4. **Competitors**: leaderboard table (mentions out of N prompts) plus a board by pricing model.
5. **Sources**: table grouped by type, then table grouped by prompt (no boards with many empty columns).
6. **Articles**: table grouped by prompt plus a shipping board.
7. **Discussions**.
8. **Listings and mentions**.
9. Raw databases.

### Six databases
- **Prompts**: Prompt, Engine, AIO shown, CursorClip named, cited, In the AI answer? (Not in the answer / Partly in the answer / Named in the answer), Google position, Impressions, Clicks, Tools listed, Conditions, Last checked, Audit doc, Status.
- **Competitors**: Tool, Prompts it appears in, Mentions (rollup), Pricing model, Price the AI showed, Own page or channel cited, Why it gets in, Price verified. Include a reference row for the client product.
- **Sources**: Source, Link, Prompt, Domain, Type, Feeds, Seen on, Device, Status, Link verified.
- **Articles**: Action, Prompt, Track, Type, Target URL, Why, Priority, Effort, Status (Not started / Drafting / Ready to ship / Shipped / Skipped), Ship date.
- **Discussions**: Thread, Link, Prompt, Platform, Open to comment, Action, Plan, Status, Date.
- **Listings and mentions**: Website, Link, Prompt, Type, Feeds, Action, Cost, Status, Date.
Every row in Articles, Discussions, Listings and Competitors has a page body (side page) with why, how, evidence, and an AI prompt.

### Repeating it: duplicate, do not rebuild
1. Keep one clean master copy of the page (empty rows, schema intact).
2. For a new client, duplicate the master, rename, and clear the rows.
3. Duplicating creates new databases with new IDs. Re-fetch the page to get the new IDs before editing.
4. Daily: edit rows only. Never rebuild the page.

### Gotchas I hit
- Notion free plan allows one chart. Use boards grouped by select properties instead. Boards cannot group by a rollup.
- A column chart needs a GROUP BY.
- Replacing page content fails if it would delete child databases. Include their tags, or confirm deleting only a view you are replacing.
- Removing a select option removes its values. Reassign rows first.
- Renaming a select and altering its options in one step created a duplicate column. Rename, then alter, then drop the stray column.
- Rows made by an AI can contain wrong ids: always copy page ids from a query, never type them.
- Competitor prices the AI showed are not verified. Keep "Price verified" unchecked until checked.

## PART B. AI AGENT INSTRUCTIONS

**Role:** Notion tracker builder and updater. You use the Notion tools. You never delete data you did not create.

### Mode 1: Build from scratch
1. Create the six databases with the schemas above. Link Prompt relations from Articles, Discussions, Listings, Sources and Competitors to Prompts (Competitors dual).
2. Create rows from the audit docs and capture log.
3. Create views: leaderboard table and pricing board (Competitors); table and "In the AI answer?" board (Prompts); sources by type and by prompt (Sources); articles by prompt and shipping board; discussions and listings tables.
4. Compose the page in the layout order with the callout and written Overview.
5. Write a side page for every row in Articles, Discussions, Listings and Competitors (SOP 03 template).
6. Verify: open the page, check that every link in Sources exists, no personal names, no contact details, no client team member names.

### Mode 2: Duplicate for a new client
1. Duplicate the master page.
2. Wait until copy placeholders resolve. Fetch the page and record the new collection URLs and view URLs.
3. Clear rows. Re-run SOP 01 to 03 for the new client. Fill the rows.

### Mode 3: Daily refresh
Input: today's capture rows, any status changes, any new sources.
1. Update Prompts rows: In the AI answer?, Last checked, Tools listed, Conditions.
2. Add new Sources rows or mark dropped sources (Status).
3. Add new Competitors or update Price verified.
4. Update Articles Status and Ship date for shipped fixes. One fix per day.
5. Update Discussions or Listings Status and Date.
6. Update the Overview findings only if a pattern changed. Do not rewrite everything.
7. Report a change log: row, old value, new value.

**Rules:**
- Query rows with SQL or rows mode to get ids. Never type ids.
- Use the schema names exactly. Property names "id" and "url" need the `userDefined:` prefix.
- Checkboxes use `__YES__` and `__NO__`. Dates use `date:Prop:start`.
- Do not delete a database or view without saying exactly what will be removed.
- No personal names or contacts in any row.

**Done when:** the page loads, every row opens a side page with an AI prompt, and the change log matches the capture log.
