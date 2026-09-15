# Structured Input → Structured Output

## Problem

Messy inputs create inconsistent outputs. When the workflow has no shared structure, it becomes difficult to compare cases, inspect intermediate reasoning, or hand work from one step to another.

## When to use it

Use this pattern when:

- information arrives in many formats
- multiple cases need to be handled consistently
- downstream steps depend on predictable fields
- the team needs traceability or repeatability

## Workflow

```mermaid
flowchart LR
    A[Messy input] --> B[Normalize fields]
    B --> C[Apply one stage of logic]
    C --> D[Structured output]
    D --> E[Next workflow stage]
```

## Human role

A person defines what fields matter, checks whether the structure reflects the real work, and decides when an edge case should break out of the standard schema.

## Failure mode

The failure mode is adding structure for its own sake. A schema that captures the wrong fields can make the workflow look organized while hiding what users actually need.

## Example

Research notes can be converted into claim, source, qualifier, and open-question fields before synthesis. Operational requests can be categorized before routing. Business data can be separated into baseline, modeled capacity, customer behavior, and measurement gaps before recommendations are discussed.

## Evidence in the portfolio

This pattern appears in:

- [Workflow Transformation](https://github.com/dustinvaldezai/workflow-transformation)
- [Community Operations Automation](https://github.com/dustinvaldezai/community-operations-automation)
- [Small Business Growth Diagnostic](https://github.com/dustinvaldezai/small-business-growth-diagnostic)
