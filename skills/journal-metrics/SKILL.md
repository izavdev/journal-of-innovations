---
name: journal-metrics
description: Turn vague improvement claims into relevant numerical metrics with explicit rationale, reproducible collection methods, guardrails and an honest expected-versus-observed comparison.
---

# Metric design guide

Use `docs/approach.md` from a local Journal of Innovations checkout when available. Otherwise, read [the shared approach](https://github.com/izavdev/journal-of-innovations/blob/main/docs/approach.md). Also read the measurement-contract section of [the entry template](references/journal-entry.md) bundled with this skill.

## Workflow

1. Clarify what “better” means for the affected person: elapsed time, active effort, defects, cost, predictability, perceived burden, or another outcome. Do not assume these are interchangeable. Record the user’s estimated magnitude and whether it predates results.
2. Map change → behavior → outcome. Suggest two to four candidate metrics in a compact table: metric, why relevant, source feasibility, proxy limitations, possible distortions. Recommend one primary outcome and usually one or two supporting/guardrail metrics. Explain rejected attractive-but-weak measures such as adoption counts used as proof of effectiveness.
3. Check feasibility against actual available sources. Ask for field definitions or a small sample when necessary. A plausible query is a proposed query until checked. If no source exists, propose a manual pilot with exact collection instructions; leave numbers pending.
4. Complete every measurement-contract field: formula, units, aggregation, direction, observation unit, population, exclusions, denominator, source and retrieval, event boundaries, timezone, windows, maturity, cadence, owner, missing/duplicate rules, limitations, and dry run. Explain consequential choices instead of filling them arbitrarily.
5. Check denominator and case-mix stability. More total bugs can reflect more releases; lower average duration can reflect easier work. Define comparable exposure and capture relevant mix. Preserve extreme cases unless an advance eligibility rule excludes them. Specify treatment of unfinished cases so only counting quick completions cannot quietly improve the result.
6. Recommend a minimum worthwhile change based on cost and user value; get it confirmed before calling it agreed. Choose a window that fits outcome latency and normal variability. Do not invent a universal sample size. Formal precision or causal requirements need an explicit analysis plan.
7. Walk through one calculation using supplied data or clearly labeled synthetic numbers. Show original values, absolute change and relative change. For rates distinguish percentage points from percentages. If the baseline is zero, report relative change as undefined. Do not apply relative percentages blindly to negative or arbitrary-scale values.

## Output

Return the candidate comparison, selected metric contracts, unresolved collection gaps, and a short explanation of how each metric tests the hypothesis. Keep a separate expectation line, such as “expected 30% reduction; basis: intuition.” If measured improvement is 5%, report 5%. Ask whether the feeling concerns a different outcome only as a new hypothesis; never swap the primary metric to rescue success.

Numbers do not eliminate bias. Surveys are valid measures of reported experience when administered consistently, but are not direct measures of productivity. Do not claim an observed difference is reliable from two aggregate values alone. Preserve missingness, counts and available spread for review.
