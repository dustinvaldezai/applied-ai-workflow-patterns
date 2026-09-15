# Applied AI Workflow Patterns

A small library of reusable workflow patterns drawn from applied AI work in research, operations, and business diagnosis.

This repository is not a framework for building autonomous agents or a claim of software-engineering depth. It captures recurring design choices I use when AI is part of real operational work: make the problem explicit, structure the workflow, preserve uncertainty, keep human judgment where it matters, and design outputs that can actually be used.

## Why this exists

The case studies in my portfolio show different contexts:

- [Workflow Transformation](https://github.com/dustinvaldezai/workflow-transformation) — research, evidence validation, synthesis, and review
- [Community Operations Automation](https://github.com/dustinvaldezai/community-operations-automation) — recurring operations, routing, approval, and follow-up
- [Small Business Growth Diagnostic](https://github.com/dustinvaldezai/small-business-growth-diagnostic) — operational data, scenario modeling, limitations, and decision support

This repository extracts the patterns that repeat across those projects.

## Pattern library

| Pattern | Core idea | Useful when |
| --- | --- | --- |
| [Human Review Gate](patterns/human-review-gate.md) | AI can prepare work without owning the final judgment | errors or commitments have meaningful consequences |
| [Evidence Before Synthesis](patterns/evidence-before-synthesis.md) | Validate inputs and claims before asking for conclusions | research, analysis, or recommendations depend on source quality |
| [Keep Unknowns Visible](patterns/keep-unknowns-visible.md) | Uncertainty should remain explicit instead of being smoothed away | data is incomplete, directional, modeled, or contradictory |
| [Structured Input → Structured Output](patterns/structured-input-structured-output.md) | Constrain messy work into inspectable stages and schemas | consistency, traceability, and repeatability matter |
| [Fail Toward Review](patterns/fail-toward-review.md) | Ambiguous or higher-risk cases should stop rather than force automation | routing, messaging, decisions, or exceptions require judgment |
| [Diagnose Before Intervention](patterns/diagnose-before-intervention.md) | Separate problem validation from solution selection | teams are tempted to jump directly from symptoms to tactics |

## How to use the patterns

Each pattern uses the same structure:

**Problem → When to use it → Workflow → Human role → Failure mode → Example → Evidence in the portfolio**

They are deliberately tool-agnostic. The useful part is the operating logic, not whether a specific step happens in ChatGPT, a spreadsheet, an automation platform, or another system.

## Portfolio evidence map

See [evidence-map.md](evidence-map.md) for where each pattern appears in the three case-study repositories.

## A practical operating thesis

AI should make work clearer, more reliable, and easier to act on.

That usually means resisting two shortcuts:

1. asking one model call to do the entire job
2. treating speed as success before the output is inspectable and usable

A good workflow creates enough structure that a person can understand what happened, see what remains uncertain, and intervene when judgment is required.

## Scope

This is a public portfolio artifact. Examples are generalized from demonstrated workflow choices in the linked repositories. It does not expose confidential client data, proprietary prompts, private records, or internal organizational rules.

No code is included because the patterns are about workflow design and decision boundaries. Code should be added only when it materially improves the system rather than serving as technical decoration.
