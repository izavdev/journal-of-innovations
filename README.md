# Journal of Innovations

Every change is a hypothesis. Measure it consistently, make a proportionate decision, and preserve what you learned.

This repository shares Ivan Zavialov’s concept and practical approach to evaluating changes in how we work. An innovation can be a tool, checklist, process, rule, or ritual. The journal records the expectation, evidence, limits, and decision—not just successful ideas.

It is a method and a toolkit, not an application. Use a document, spreadsheet, issue tracker, or whatever interface suits your team. The HTML is a portable concept overview, not the journal’s storage format.

## Start here

1. Open [the concept overview](journal-of-innovations.html) in a browser.
2. Read [the approach](docs/approach.md), including how to separate perception, measurement, and attribution.
3. Copy [the entry template](templates/journal-entry.md), or work through it with the skills below.
4. See [a worked example](examples/review-checklist.md) where an expected 30% improvement turns out to be 5%.
5. Compare [good and bad entries](examples/good-and-bad.md) for the same change, with an explanation of each difference.

## Guided skills

These are portable Markdown instructions for an AI assistant. They guide a conversation, explain choices, and produce reviewable journal records. They do not connect to your systems or invent measurements.

| Skill | Use it when | Result |
|---|---|---|
| [Journal entry](skills/journal-entry/SKILL.md) | You have an idea or want to record an existing change | A draft entry, comparison design, and collection plan |
| [Journal metrics](skills/journal-metrics/SKILL.md) | You need to turn “better” into something measurable | Metric definitions with rationale, formulas, and limitations |
| [Journal review](skills/journal-review/SKILL.md) | You have results and need to decide what they mean | A numerical comparison, evidence limits, and a decision |

For an assistant that supports `SKILL.md` packages, copy the desired skill directory into its configured skills location, following that assistant’s instructions. Keep this repository accessible: the skills use its approach and template, with relative paths when run in place. If installed separately, provide the repository path. No installation is required to use the guidance manually.

Example prompt:

> Use skills/journal-entry/SKILL.md in this repository to help me evaluate a new code-review checklist. I think it will make reviews 30% faster. Help me define what “faster” means, choose defensible measurements, and explain what the evidence could actually establish.

## What good looks like

Someone else can reproduce the measurement. The metric represents an outcome that matters. Expectations and success criteria predate the results. The conclusion says what was observed without claiming more than the design supports. A decision can be provisional; an inconclusive experiment is a valid entry.

The assistant should do the drafting and arithmetic, ask focused questions, and explain why each important choice matters. The user supplies context and verifies the plan. A polished record with invented numbers is a failure.
