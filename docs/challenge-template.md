# Challenge: <name> (<date>)

## Incident summary

- The alert: what triggered it (IDS rule, suspicious process, phish report...)
- Verdict: true positive / false positive + one-line explanation.

## Investigation timeline

- Step 1: filter/query I used (exact KQL/SPL/Lucene syntax) + what it showed.
- Step 2: what I pivoted to next and why (field, indicator, sandbox...).
- Each step: what I looked for -> what I found -> what decision it drove.

## Indicators of Compromise (IoCs)

| Type        | Value | Source                       |
| ----------- | ----- | ---------------------------- |
| user-agent  | ...   | connection logs              |
| IP / domain | ...   | VirusTotal / Hybrid Analysis |

## MITRE ATT&CK mapping

- T-ID — technique name — the exact log evidence that matches it.

## Recommendations

- What the SOC should block/detect going forward (rule, control, follow-up).

## What was hard / What I learned
