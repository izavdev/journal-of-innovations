# The approach

## Purpose

Make changes deliberately, evaluate them honestly, and build shared memory. The journal helps decide what to keep, adjust, or roll back. It does not promise that every workplace change can become a controlled experiment.

## Separate three questions

1. **Perception:** What do we expect or feel? Record this before inspecting results when possible. An estimate such as “30% faster” is an expectation, not evidence.
2. **Measurement:** What changed in the defined outcome? Preserve the source, formula, observations, and periods so another person can reproduce the result.
3. **Attribution:** How much can we reasonably connect to the innovation? Consider what would have happened without it and what else changed.

If the change has already happened, label the entry retrospective. Do not recreate a supposedly advance prediction or invent a baseline. Historical data is useful only if its definitions and coverage are comparable; otherwise collect a new baseline for a future test.

## Choose metrics for a reason

Start with the person affected and the outcome that matters to them. Write the chain: change → expected behavior → useful outcome. Select one primary outcome metric and, usually, one or two supporting or guardrail metrics. A guardrail tracks a cost you refuse to hide, such as errors increasing while work becomes faster.

For every candidate, explain:

- **Relevance:** Which part of the hypothesis does it test, and why would movement matter?
- **Validity:** Does it measure that outcome directly, or only a proxy? More checklist completions show adoption, not fewer bugs.
- **Reproducibility:** Can another person collect and calculate it from the definition?
- **Sensitivity:** Could it reveal the smallest improvement worth acting on within a practical observation period?
- **Failure modes:** Could workload, case mix, missing data, gaming, or a changing denominator improve the number without improving the outcome?

Do not select a metric merely because it is available. If no credible measure exists, mark the hypothesis not yet measurable and propose a small collection pilot. Numbers are not automatically objective: a survey can measure perceived effort, but does not establish time saved. Measure both separately if both matter.

## Make a measurement contract

For each metric, specify its name, role, units, direction, formula and aggregation; source and exact fields or query; eligible population, exclusions and denominator; event start/end definitions; timezone and window boundaries; collection frequency; missing-value and duplicate handling; owner; and known limitations.

Choose aggregation deliberately. A mean answers an average question; a median describes the middle observation and can hide extreme delays. Keep the definition fixed and retain counts and spread where available. If comparing rates, report both numerator and denominator. Avoid combining percentages with different denominators by simply averaging them.

Use comparable windows, with the same duration or exposure definition, and account for seasonality, workload and outcome maturity. Four releases are not necessarily comparable if their size or bug-discovery time differs. Define any rollout or learning period before seeing outcomes. If the method changes, version it and recompute both periods if possible; otherwise mark a break in comparability.

A dry run should retrieve real observations and demonstrate the formula before the plan is considered ready. Mark unavailable data explicitly. Agree on a review date and collection window in advance; do not stop at the first favorable result or extend only until a target is met. A follow-up can be a new, recorded experiment.

## Match the comparison to the decision

| Design | Plan | Limits and appropriate language |
|---|---|---|
| Before / after | Observe the same population with consistent definitions across comparable periods | “The metric changed after introduction.” Time trends and other changes can explain it. |
| Comparison group | Observe an untreated comparable group over the same periods; inspect its earlier trends and relevant differences | “The observed change exceeded that in the comparison group.” Attribution depends on comparable trends and no important differential shocks or spillovers. |
| Randomized trial | Specify eligible units, random assignment, control condition, exposure, duration, and analysis before rollout | Can support a causal estimate when assignment and analysis are sound. Small samples, missing outcomes, contamination and non-adherence still matter. |

Randomize at a level that limits spillovers: people sharing a checklist may contaminate a per-review comparison. Randomization does not guarantee a precise estimate. For costly decisions or formal causal claims, plan sample size and analysis with suitable statistical expertise rather than choosing a universal number of observations.

If a credible comparison is impractical, state why and narrow the claim. A cheap, reversible change may justify a provisional decision on limited evidence; a major rollout may require a stronger experiment.

The distinction between observed change and attribution follows [HM Treasury’s evaluation guidance](https://www.gov.uk/government/publications/the-magenta-book/quality-in-policy-impact-evaluation-qpie-html). For comparison-group assumptions, see its [analytical methods annex](https://www.gov.uk/government/publications/the-magenta-book/magenta-book-annex-a-analytical-methods-for-use-within-an-evaluation-html). The journal’s templates and workflow are practical conventions, not a substitute for a statistical analysis plan.

## Check the size of the improvement

Keep the original prediction visible alongside the result. For a lower-is-better metric with a positive baseline:

`relative reduction = (before − after) / before × 100%`

For a higher-is-better metric with a positive baseline:

`relative increase = (after − before) / before × 100%`

Always show original values and absolute change too. Going from 100 to 95 minutes is a 5-minute reduction, or 5%, even if it felt like 30%. That is 25 percentage points below the predicted relative improvement. Going from a 10% error rate to 8% is a 2-percentage-point decrease and a 20% relative reduction. If the baseline is zero, relative change is undefined; use absolute change. Relative percentages may also be misleading for negative values or arbitrary-scale survey scores.

A discrepancy does not automatically mean the feeling was wrong. Perhaps the change reduced interruptions or frustration more than elapsed time. Treat that as a new hypothesis, not a replacement success metric for the completed experiment. Preserve the original outcome and label any post-hoc analysis exploratory.

## Review evidence, then decide

Report counts, coverage, missingness and available variability alongside the effect. An observed 5% shift alone does not establish a reliable improvement or “no effect.” Do not invent confidence intervals or significance from aggregate values without the required data and assumptions. A success threshold describes practical value; it is not a statistical certainty threshold.

List alternative explanations, the evidence for each, and what could distinguish them. Describe confidence in plain language tied to the design and data; do not assign a fabricated probability.

Close with: observed result; whether the advance target and guardrails were met; attribution limits; and keep, adjust, roll back, or inconclusive/collect more. Include the owner, next review date or condition, costs and reversibility. Keep failed and inconclusive entries. Preserve the original plan and append dated amendments rather than rewriting history.
