# survey-findings-report

Turns a raw survey export (CSV) into the Word findings report a research freelancer would hand back: answer counts for every question, open-text answers grouped into themes, charts, real quotes and three recommendations, with every number rechecked against the file.

It asks the questions your material leaves open (each with a default) before it builds anything, then runs a "Done means" check and reports the result.

## Install

- Upload `survey-findings-report.zip` in your Claude skills settings, or
- Copy this folder into `~/.claude/skills/survey-findings-report/` (Claude Code), or
- `npx skills add arm-pz/survey-findings-report`

Check: start a new session and confirm `survey-findings-report` appears in the skill list.

## Try it

- "Write up our customer survey results for the board, the CSV is survey.csv."
- "Turn these Google Form responses into a report I can send to my manager."

## Boundaries

See the description in `SKILL.md`: the "Not for" clause names which skill takes each excluded request.

## Test results

Version 0.1.0: 3 pass, 1 fail executed live. Details in `TEST-CASES.md`.

## Credits

Prompt adapted from the freelancer workflows thread by @claudeskills101 on X.

## Version

See CHANGELOG.md.
