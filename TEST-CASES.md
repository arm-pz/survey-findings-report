# Test cases: survey-findings-report

## Executed (2026-11-13)

Claude Code 2.1.323, skill installed in a fresh project next to other skills (docx, pptx, xlsx, pdf, design, searchfit-seo, remotion), each prompt sent with `claude -p` in a new session; first Skill call recorded.

| Prompt | Expected | Loaded | Result |
| --- | --- | --- | --- |
| Write up our customer survey results for the board, the CSV is survey.csv. | should load | survey-findings-report | pass |
| We asked 200 members about the new class timetable, here's the export, what should I tell the committee? | should load | none | FAIL (no file was attached in the test, so the session asked for it first) |
| Turn these Google Form responses into a report I can send to my manager. | should load | survey-findings-report | pass |
| Help me write good questions for a customer survey. | should not load | design:user-research | pass |

**3 pass, 1 fail.**

## Reviewed only (read from descriptions, not executed)

| # | Type | Message | Expected | Result |
|---|---|---|---|---|
| 1 | C | "Write up our survey results for the board, CSV attached" | survey-findings-report | pass |
| 2 | C | "Turn these Google Form responses into a report" | survey-findings-report | pass |
| 3 | C | "What did customers say in this feedback export?" | survey-findings-report | pass |
| 4 | I | "We asked 200 members about the new timetable, here's the export, what's the takeaway?" | survey-findings-report | pass |
| 5 | I | "Our NPS responses are in this file, can you make something I can send my manager?" | survey-findings-report | **weak**: design:research-synthesis also matches NPS; acceptable, the CSV + "send" leans here |
| 6 | N | "Remove the duplicate rows in survey.csv" | xlsx | pass |
| 7 | N | "Help me write survey questions for customers" | design:user-research | pass |
| 8 | N | "Build a live dashboard from our survey data" | Dashboard artifact type | pass |
