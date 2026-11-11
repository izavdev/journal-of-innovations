# Good example / bad example

A good entry can record a disappointing result. A bad entry can describe a genuinely useful change but provide no trustworthy way to assess it.

Both versions below concern the same code-review checklist. All numbers are synthetic. The good version summarizes the [full worked example](review-checklist.md); its measurement definitions and limitations apply here too.

## Bad example: a convincing story

> We introduced a review checklist to improve productivity. Reviews feel about 30% faster, and everyone seems happier. Forty reviews used the checklist, which proves it works. Average waiting also fell from 20 to 19 hours. Any improvement counts as success, so we should roll it out to every team.

This sounds positive, but it confuses an impression, adoption, a measured outcome and a causal claim. It also replaces the original 15% success threshold with “any improvement.”

## Good example: a useful record

> Before rollout, we predicted a 30% reduction in mean waiting time to first substantive review, based on intuition. We set a minimum worthwhile reduction of 15%, with no increase in seven-day corrective-follow-up rate.
>
> We chose waiting time because authors need timely feedback. Checklist usage measures adoption; it cannot tell us whether feedback arrives sooner. Waiting time also does not measure reviewer effort or frustration.
>
> We used the same review log and definitions for requests opened in two 28-day windows for the same team. Each request received seven days of follow-up. We averaged elapsed hours to first substantive human review, capped at 168 hours, with unreviewed requests contributing the cap. We retained source records and reported missingness and the number reaching the cap.
>
> Across 40 eligible requests in each period, mean capped waiting fell from 20 to 19 hours: 1 hour, or 5%. The predicted 30% reduction would have meant 14 hours; the 15% success threshold required 17 hours or less. The target was missed. Corrective follow-ups remained 4/40 in each period; that is no observed increase, not proof that quality is unchanged.
>
> This was a before/after comparison without an independent comparison group. Request complexity was not measured, so easier work could explain some or all of the change. The aggregate results do not establish precision or isolate the checklist’s contribution.
>
> Keep provisionally because the owner judges upkeep low and the change is reversible. The review process lead will reassess on 15 December under a new plan that captures workload mix and upkeep. Easier-feeling reviews are a separate hypothesis to investigate, not a reason to relabel this experiment successful.

## What makes the difference?

| Choice | Bad example | Good example | Why it matters |
|---|---|---|---|
| Hypothesis | “Improve productivity” | Reduce a specific waiting-time measure through a stated change | Makes the expectation testable |
| Metric relevance | “40 reviews used it, so it works” | Waiting measures feedback delay; usage measures adoption | Activity is not evidence of the intended benefit |
| Measurement | “Average waiting went down” | Same source, population, windows, event definitions and aggregation; unfinished cases handled explicitly | Another person can reproduce the comparison |
| Expected magnitude | Feeling becomes “30% faster” | 30% is a dated prediction; 5% is the measured reduction | Keeps perception separate from evidence |
| Success criteria | “Any improvement counts” after seeing results | Preserve the advance 15% target and report it missed | Prevents moving the goalposts |
| Side effects | “Everyone seems happier” | Defined quality guardrail, with its limits acknowledged | Prevents one favorable metric hiding costs |
| Comparison design | Improvement proves causation | Before/after supports an observed change, with attribution uncertain | Keeps the claim within the design’s reach |
| Alternative explanations | Ignore easier requests | Identify missing complexity data and collect it next time | Makes competing explanations actionable |
| Evidence limits | Treat two averages as conclusive | State that precision and causal contribution remain uncertain | Avoids false certainty |
| Decision | Roll out everywhere | Provisional decision with rationale, owner and review date | Separates a practical choice from proof of success |

## If you already wrote the bad version

Preserve it and append a dated correction. Retrieve comparable historical data if available; mark absent measurements unknown. If there was no advance target, say so rather than inventing one. Set a prospective target for the next experiment. A retrospective entry can still be useful when its limitations are explicit.

When using the guided skills, ask the assistant to identify the specific weakness, explain its consequence, and draft a correction using only known facts. Missing facts should become focused questions or collection tasks, not plausible filler.
