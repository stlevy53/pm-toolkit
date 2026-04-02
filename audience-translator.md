# Audience Translator

## Problem

PMs rewrite the same information multiple times per week for different audiences — eng gets the spec, leadership gets the summary, stakeholders get the update, customers get the changelog. Each rewrite is manual, time-consuming, and introduces drift from the source of truth.

## Target User

Product managers who communicate the same initiative to 3+ audiences regularly and lose hours per week to reformatting and re-toning the same core content.

## Proposed Solution

A tool that takes a single canonical input (a PRD section, a project update, a feature description) and generates audience-adapted outputs. The user selects target audiences from a predefined set (engineering, executive, stakeholder, customer-facing) and gets tailored versions that adjust depth, tone, jargon, and structure accordingly.

## Key Features

- Accepts freeform text or markdown as canonical input
- Generates parallel outputs for 2-4 selected audience types in a single pass
- Applies distinct formatting rules per audience (e.g., exec gets a one-pager structure, eng gets acceptance criteria style)
- Allows users to define custom audience profiles beyond the defaults
- Diff view showing what changed between audience versions so the PM stays aware of what was simplified or omitted

## Open Questions & Tradeoffs

- CLI tool vs. web UI vs. both (like doc-to-markdown)? Web UI probably has broader appeal for non-technical PMs.
- How opinionated should the audience profiles be? Too generic and the output is useless; too rigid and it won't match how different orgs communicate.
- Should it support iteration — take feedback on one output and adjust — or is single-pass generation enough for v1?

## Scope

Weekend build for a CLI version with hardcoded audience profiles. Multi-session if it includes a web UI, custom profiles, and the diff view.
