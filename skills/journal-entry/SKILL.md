---
name: journal-entry
description: Guide a user from a proposed or existing workplace change to a reproducible Journal of Innovations entry, including hypothesis, metrics, comparison design, alternative explanations and evidence limits.
---

# Journal entry guide

Use this when the user wants to document or plan an innovation experiment. Produce a record, not an app or dashboard.

## Reference material

Read `../../docs/approach.md` and `../../templates/journal-entry.md` relative to this skill directory. If installed outside the repository, use the repository location supplied by the user; if unavailable, ask for it rather than silently assuming access. Use the sibling `journal-metrics/SKILL.md` for metric design and `journal-review/SKILL.md` for existing results. Follow their guidance within the conversation; no separate agent is required.

## Conversation

1. Extract what the user already provided. Ask at most three focused questions per round, starting with the change, intended beneficiary/outcome, and whether implementation or result inspection has already happened. Explain briefly why missing information matters. Do not present the entire template as a questionnaire.
2. Draft the hypothesis and mechanism in the user’s language. Separate a perceived improvement or predicted magnitude from measured evidence. Ask what makes the expected magnitude plausible; “intuition” is an acceptable labeled basis.
3. Apply the metric skill. Offer reasoned candidates, recommend a small set, and produce reproducible definitions. Never fabricate source fields, queries, baseline values, dates or thresholds. Clearly label proposed choices until confirmed.
4. Help choose a comparison design proportionate to the decision. Explain what each feasible option could establish. For comparison groups specify selection, prior trends and concurrent conditions; for randomization specify unit, allocation, spillover risks and analysis needs. If neither is feasible, use before/after and narrow the claim.
5. Surface plausible alternative explanations specific to this change. For each, propose an observable check, such as release size, staffing, workload mix or seasonal demand. Do not declare them ruled out without evidence.
6. Agree on the minimum worthwhile improvement, guardrails, window, owner and review trigger before rollout. Explain the tradeoff behind each proposal. Do not present a practical success threshold as proof of causality or statistical significance.
7. Return a draft using the repository template. Include a concise readiness assessment and the next concrete collection action. Mark ready only when the method can be executed, a dry run is documented, and material plan choices are confirmed. Otherwise preserve useful work and list specific gaps.

## Quality bar

The user should understand why the outcome matters, why the metric represents it, how to collect it, what could mislead them, and what conclusion the design permits. Do the synthesis and drafting for them. Preserve existing entries and append dated amendments; never rewrite a prior prediction after results are known. Retrospective entries must say so. Do not collect or transmit data without authorization.
