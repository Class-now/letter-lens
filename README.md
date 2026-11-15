# Letter Lens — short introduction (English, for the submission form)

**Quest:** AI for Good (University)
**Team:** 1 person

## What it is
Letter Lens explains Japanese official letters — pension slips, tax bills, health-insurance notices, garbage rules, immigration letters — to international students and residents in plain English: what the letter is, what to do, by when, and who to ask. When a wrong answer could hurt (a torn slip, a scam, a seizure warning, a refusal, an immigration letter about a pending application), it does not guess: it tells the reader which person or office to talk to first.

## Why
About 3.8 million foreign residents live in Japan (Immigration Services Agency, end of 2024), and almost every one of them receives letters written only in formal Japanese. As a foreign-languages student in Tokyo I see international classmates photograph these letters and ask friends what they mean. When I turned 20 I had to work out a pension letter myself, in my own language, and it was still hard. A reader who misses a deadline loses money; a reader who trusts a wrong answer on an immigration letter can lose much more.

## What I built and tested
- Three prompt versions (v1–v3) on Claude, each changed by a rule I wrote after reading the failures.
- 44 invented, realistic letters with an answer key: 26 main, plus two held-out sets written before the version they test was run. 15 of them must be handed off to a person.
- Success targets fixed before the first run. v3: letter type 96% (main), deadline 100%, action coverage 100%, hand-off 15/15, 0 false hand-offs on 44 letters, no invented dates, reading level FK grade about 5.
- A one-page demo judges can open without an API key, showing every letter, the v3 and baseline answers, and the scores.

## Responsible AI
No real personal data. Dates and amounts that are not printed are never guessed. High-stakes letters go to a person, and false alarms are counted so the warning stays meaningful. Scams: do not pay; call the ward office or the police line #9110. Limits: tested on invented letters from one fictional ward; real letters vary by city. It is a reading aid, not legal advice.

## Tools used
Claude Code and Claude (Anthropic): drafting the letters and scripts, running the prompts, building the demo page. My decisions: the user group, the risky cases, the success targets, every rule change, and what to report as a weakness.
