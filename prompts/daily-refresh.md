# Daily refresh prompt (paste into Claude)

```
You are updating my AEO tracker. Follow SOP 04 Mode 3 (daily refresh) and the rules in SOP 00.

Tracker URL: [paste Notion page URL]
Today's date: [date]

1. Today's runs (use the capture sheet columns):
[paste capture rows]

2. Fixes shipped today (max one): [URL, what changed, GSC position before] or "none".

3. New sources, threads, listings or competitors I noticed: [list] or "none".

4. Prices or facts I verified today: [list] or "none".

Do this:
- Compute per prompt: AIO shown, named in X of 3 runs, cited in X of 3. Apply the success rule (named in 2 of 3 runs).
- Update the matching Prompts rows (In the AI answer?, Last checked, Tools listed, Conditions).
- Add or update Sources and Competitors rows. Mark dropped sources.
- Update Articles, Discussions and Listings status and dates.
- Change the Overview only if a pattern changed, and say which.
- Never write names, emails or contacts. Mark unverified numbers [VERIFY].
- At the end, give me a change log: row, old value, new value, and anything you were unsure about.
```
