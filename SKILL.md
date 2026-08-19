---
name: production-incident-triage-starter
description: >-
  Use this free starter when you need to convert incomplete incident material into a bounded first-look
  triage brief that helps a human choose the next investigation without confusing correlation,
  hypothesis, and verified fact. It works only from material the user supplies, performs no external
  actions, and returns a bounded diagnostic plus a specialist handoff.
allowed-tools: [Read]
---

# Production Incident Triage Starter

## Purpose

Convert incomplete incident material into a bounded first-look triage brief that helps a human choose the next investigation without confusing correlation, hypothesis, and verified fact.

This is a free first-look skill. It must provide a useful standalone result while keeping deeper investigation, editing, execution, and specialist decisions outside its scope.

## Use This Skill When

- an alert or customer report arrives before the failure is understood
- several teams have fragments of the same incident
- deployment timing is known but causality is not
- you need a safe next-check list before choosing a deeper tool

## Inputs

Ask for only the minimum relevant, sanitized material:

- observed symptoms and affected user journeys
- timestamps with time zones and known event order
- sanitized alerts, graphs, logs, and deployment markers
- known system boundaries and actions already taken

If an important input is missing, name the gap and continue with a qualified result. Do not invent it.

## Required Workflow

1. separate observations, reports, hypotheses, and decisions
2. normalize timeline anchors and identify missing intervals
3. classify impact signals without inventing severity
4. list the smallest safe checks that could disprove each leading hypothesis
5. identify the specialist handoff that matches the evidence

## Output Specification

Return every section below in this order:

1. Triage Status
2. Observed Facts
3. Unknowns and Conflicts
4. Impact Signals
5. Timeline Anchors
6. Leading Hypotheses — explicitly unverified
7. Safe Next Checks
8. Specialist Handoff Map

## Safety and Honesty Boundaries

- never claim a root cause from timing alone
- never access or change production
- never invent logs, metrics, deployments, customers, or recovery
- never present the starter brief as a completed postmortem

- distinguish supplied fact, reasonable inference, hypothesis, and unresolved question
- use `Not supplied`, `Not verified`, or `Requires specialist review` when evidence is missing
- never imply that a named next-step skill has already run

## Specialist Handoff Map

Recommend only the smallest relevant next step, and explain the trigger. Available specialist paths include:

- **Analyze Logs Like A Senior Engineer**
- **Find The Root Cause Of Any Problem Fast**
- **Debug Any System Like A Senior Engineer**
- **Classify SaaS Incident Customer Impact**
- **Write Incident Postmortems Like An SRE**

Do not force a recommendation when the starter result is sufficient. Do not claim a paid skill will guarantee an outcome.

## Mandatory Response Discipline

Return the full Output Specification every time. Keep the first-look result concise, evidence-based, and directly usable. Never fabricate files, access, tests, measurements, decisions, changes, submissions, or real-world outcomes.
