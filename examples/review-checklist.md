# Example: “It feels 30% faster” meets a 5% result

All dates, records and numbers below are synthetic teaching data. This demonstrates a completed review, not evidence that checklists work. No statistical significance is claimed.

## Original plan — recorded 1 September 2026

- **Owner:** Review process lead (illustrative role).
- **Change:** Introduce a code-review checklist for one team on 1 October.
- **Outcome:** Reduce author waiting time for an initial substantive review.
- **Mechanism:** A shared checklist reduces hesitation about what to inspect first.
- **Expectation:** 30% lower mean time to first review; basis: intuition from frustrating reviews, not historical evidence.
- **Success rule:** At least a 15% reduction, with no increase in seven-day corrective-follow-up rate. This illustrative threshold represents the team’s minimum worthwhile improvement given checklist upkeep; it is not a universal rule.
- **Design:** Before/after for the same team. No independent comparison team is available. Permitted claim: observed change following rollout, with causal contribution uncertain.
- **Windows:** Requests opened 1–28 September and 1–28 October, UTC; each followed for seven days. Review after 4 November. No learning-period exclusion. Record adoption and interpret early learning as a limitation.

## Measurement contracts

**Primary: mean capped elapsed hours to first substantive human review.** This directly measures waiting within seven days, not active reviewer effort or subjective ease. The synthetic source is a review log with `request_id`, `team`, `opened_at`, `first_substantive_review_at`, `is_bot`, and `corrective_followup_within_7d`. These are example fields to map to a real system, not assumed integrations.

Include all non-bot review requests for this team opened in each window. A substantive review is a human approval, change request, or comment that assesses the code; acknowledgments do not qualify. A human collector applies the same rule in both periods and retains the event reference. For each request calculate `min(hours from opening to first substantive review, 168)`. A request with no review within seven days contributes 168 hours, even if later withdrawn; it is not dropped. Compute the arithmetic mean over all eligible requests. The cap means this measures restricted waiting, not full eventual delay; also report how many requests hit it.

**Guardrail: seven-day corrective-follow-up rate.** Count requests with at least one linked correction to an issue missed in initial review within seven days of opening, divided by all eligible requests, times 100%. Use the same human classification rule and retain linked evidence in both periods. This is an imperfect quality proxy: late-discovered problems are missed and faster reviews leave more time for discovery within the window. It cannot establish production quality.

**Collection for both metrics:** Owner exports daily, deduplicates by request ID, and finalizes after every request has seven days of observation. Missing opening times or broken event histories are flagged as invalid and reported as coverage gaps, never converted to zero. No review is distinct from a missing event history. Retain original exports and calculation rows. Synthetic dry run: an opening at 10:00 UTC with a substantive review at 15:00 contributes 5 hours; no review within seven days contributes 168 hours. Both definitions are executable against the synthetic log; real use requires a dry run on actual sources.

**Alternative explanations to inspect:** Request size and type, reviewer availability, holidays, workload and adoption. Collect weekly summaries of these alongside outcomes. This example lacks request-size data, so workload comparability remains unverified.

## Observed results

| Measure | Before | After | Interpretation |
|---|---|---|---|
| Eligible requests | 40 | 40 | All synthetic records have complete event histories |
| Total capped waiting hours | 800 | 760 | Same method and eligible population definition |
| Mean capped waiting hours | 20 | 19 | 1 hour lower; `(20 − 19) / 20 × 100 = 5%` reduction |
| Requests reaching seven-day cap | 2/40 | 2/40 | Same count; long delays still matter |
| Corrective-follow-up rate | 4/40 = 10% | 4/40 = 10% | No observed increase; uncertainty remains |

The expected 30% reduction would have produced 14 hours. The success threshold of 15% required 17 hours or less. The observed 19 hours is a 5% reduction, 25 percentage points below the expected relative reduction, and misses the advance target.

**Perception after rollout:** The owner still reports that reviews feel much easier. That could concern mental effort or interruptions, which these metrics do not measure. It motivates a separately planned study of perceived effort; it does not change this experiment’s target.

## Evidence and limits

The observed time metric improved by 5%. The aggregates alone do not tell us whether this is distinguishable from normal variation; raw observations would be needed for a justified uncertainty analysis. Equal sample counts do not guarantee equal complexity. Without a comparison group, and with request size unmeasured, we cannot isolate the checklist’s effect. The quality proxy also has limited follow-up and does not demonstrate unchanged long-term quality.

## Decision

**Keep provisionally, without declaring success.** The original improvement target was missed. The owner judges the checklist inexpensive and easy to reverse; this is an operational judgment, not a measured benefit. Keep it until a follow-up review on 15 December 2026, owned by the review process lead, with workload mix and maintenance effort collected under a new dated plan. If a credible comparison becomes feasible, specify it before collection. Preserve this entry as a missed target with uncertain attribution.
