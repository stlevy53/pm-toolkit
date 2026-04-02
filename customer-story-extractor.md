# Customer Story Extractor

## Problem

Customer insights are trapped in unstructured artifacts — research interview notes, support tickets, sales call transcripts, feedback surveys. PMs know the signal is in there but extracting structured, reusable customer stories requires hours of manual synthesis. Most of this work gets done once, poorly, or not at all.

## Target User

PMs who have access to raw customer data (transcripts, tickets, notes) and need to turn it into structured stories they can use in PRDs, prioritization discussions, and stakeholder communication.

## Proposed Solution

A tool that ingests unstructured customer input (pasted text, uploaded documents) and extracts structured customer stories. Each story follows a consistent format: persona, problem, current workaround, desired outcome, and emotional context. The PM reviews, edits, and approves extracted stories, building a searchable library over time.

## Key Features

- Accepts multiple input formats: pasted text, markdown, uploaded transcripts or documents
- Extracts one or more customer stories per input, each with structured fields (persona, problem, workaround, desired outcome, context/sentiment)
- Confidence flagging — marks extracted fields as strong or inferred so the PM knows what needs human validation
- Searchable story library that accumulates across sessions
- Export individual stories or batches to markdown for inclusion in PRDs or presentations

## Open Questions & Tradeoffs

- How to handle inputs where the customer story is implicit or ambiguous? Aggressive extraction risks fabrication; conservative extraction misses signal.
- Should persona mapping be freeform or use a predefined persona framework? Freeform is flexible; predefined enables cross-story analysis.
- Story deduplication: if multiple inputs describe the same underlying problem, should the tool detect and merge them? High value, high complexity.
- Privacy considerations for storing customer data — even locally, this needs thought.

## Scope

Weekend build for single-input extraction with markdown export. Multi-session to add the persistent story library, deduplication, and confidence scoring.
