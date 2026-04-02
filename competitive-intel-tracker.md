# Competitive Intel Tracker

## Problem

Competitive landscape documents are born as slides or spreadsheets, go stale within weeks, and live in places nobody revisits. The research process is manual and repetitive — the same PM re-Googles the same competitors every quarter and rebuilds the same comparison matrix from scratch.

## Target User

Product managers responsible for competitive positioning, particularly those managing platforms or tools where the competitive set shifts frequently (new entrants, feature parity changes, pricing moves).

## Proposed Solution

A structured competitive tracking tool that maintains a living comparison matrix. Users define competitors and evaluation dimensions, input findings through structured entries, and get an always-current view of the landscape. AI assists by summarizing findings, identifying gaps in coverage, and flagging when an entry is aging out.

## Key Features

- Structured data entry for competitor profiles (positioning, pricing, key features, strengths, weaknesses)
- Comparison matrix view that surfaces gaps and highlights recent changes
- Staleness detection — flags entries that haven't been updated beyond a configurable threshold
- AI-generated summaries of competitive positioning based on the structured data
- Export to markdown or presentation-ready format for stakeholder consumption

## Open Questions & Tradeoffs

- Data sourcing: purely manual input for v1, or attempt to pull from web sources? Manual is simpler and more accurate; automated sourcing is higher value but much harder to get right.
- Storage: flat files (JSON/markdown) for portability, or a lightweight database for queryability?
- How to handle the "dimension" problem — every competitive analysis has different evaluation criteria. Needs to be flexible without being a blank spreadsheet.

## Scope

Multi-session. The data model and comparison views require more design iteration than a single sitting. A useful v1 with manual input and markdown export is achievable in 2-3 sessions.
