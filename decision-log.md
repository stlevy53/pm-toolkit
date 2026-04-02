# Decision Log

## Problem

PMs make dozens of scoping, prioritization, and design decisions per week. Almost none of them get recorded. Six months later, someone asks "why did we cut feature X?" or "who decided we'd build instead of buy?" and the answer lives in a Slack thread nobody can find, or in nobody's memory at all. This erodes trust and creates repeated relitigations.

## Target User

PMs and product teams who need a lightweight way to capture decisions as they happen, and who later need to recall the rationale behind past decisions — especially during retrospectives, onboarding, or stakeholder escalations.

## Proposed Solution

A lightweight decision capture tool where PMs record decisions with minimal friction: what was decided, what alternatives were considered, why this option won, and who was involved. AI assists by generating a concise summary from rough inputs and by making the log searchable. The goal is a decision journal with near-zero overhead to write and high value to read later.

## Key Features

- Quick-capture interface: accepts rough or verbose input and produces a structured decision entry (decision, context, alternatives considered, rationale, participants, date)
- Searchable log — find past decisions by keyword, topic, or timeframe
- AI-generated executive summary of any decision entry for stakeholder sharing
- Tagging and categorization (e.g., scoping, technical, prioritization, vendor) for pattern analysis
- Export to markdown for inclusion in project documentation or wikis

## Open Questions & Tradeoffs

- Input format: form-based structured capture vs. freeform text that gets parsed into structure? Freeform is lower friction but harder to parse reliably.
- Storage: local files per project, or a single persistent store across projects?
- Should it integrate with Slack (capture decisions from threads) or stay standalone for v1? Slack integration is high value but a different order of complexity.
- How to handle "living decisions" — decisions that get revisited and changed? Version history per entry, or just a new entry that supersedes?

## Scope

Weekend build for a standalone capture-and-search tool. Multi-session if it includes Slack integration or a web UI with persistent storage.
