# AI Visibility (AEO) Manual MVP: SOP Pack

Repeatable process for getting a product named in Google AI Overview answers. Built from the CursorClip run (11 to 13 Oct 2026) and written so a human can recall it and an AI agent can execute it.

## How to read each SOP
Every SOP has two parts:
- **PART A. HUMAN OVERVIEW**: what we did, why, what it looked like. Read this to recall the work.
- **PART B. AI AGENT INSTRUCTIONS**: inputs, steps, output format, rules, done-when. Paste this part (plus the inputs) into Claude.

## Files
| File | Covers |
|---|---|
| `sops/00-master-sop.md` | The whole loop, daily routine, verdict framing |
| `sops/01-keywords-and-aio-check.md` | Steps 1 and 2: find keywords in GSC, check AI Overview |
| `sops/02-reasons-and-citation-analysis.md` | Steps 3 and 4: why we are or are not named, reverse-engineer citations |
| `sops/03-opportunity-plan.md` | Step 5: turn patterns into articles, discussions, listings |
| `sops/04-notion-tracker.md` | Build, duplicate and refresh the Notion tracker |
| `prompts/daily-refresh.md` | Paste-in prompt for the daily update |
| `prompts/new-client-setup.md` | Paste-in prompt to start a new client |
| `templates/capture-sheet.md` | The run log shape (columns) |
| `templates/audit-doc-skeleton.md` | Per-keyword audit doc skeleton |
| `templates/side-page-template.md` | Row page template: why, how, evidence, AI prompt |

## Rules that apply everywhere
1. Say **observed** for what we saw, **tested** only for what we ran a controlled check on.
2. Lock the prompt list before shipping any fix. Log any scope change openly with the date and reason.
3. Separate two questions: can we improve AI visibility, and will founders pay for it.
4. No names, emails or contact details in the tracker. Websites only.
5. Disclose the founder. No fake reviews, no fake independent sites, no extra accounts. Creators must disclose free licences.
6. Never state a fact we have not verified. Mark it `[VERIFY]`.
