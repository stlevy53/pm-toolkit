# PRD Quality Scorer

## Problem

PRD quality is wildly inconsistent across teams and individuals. Most templates are checklists that ensure sections exist but say nothing about whether the content is any good. A PRD with a vague problem statement, unmeasurable success metrics, and no explicit non-goals technically passes every template check but will produce bad outcomes.

## Target User

PMs writing PRDs who want a fast quality gut-check before circulating to stakeholders, and PM leaders who want to raise the baseline quality of PRDs across their team without personally reviewing every one.

## Proposed Solution

A tool that ingests a PRD (markdown, text, or document) and scores it against an opinionated rubric of quality criteria. It doesn't check for section presence — it evaluates content quality. The output is a score breakdown with specific, actionable feedback on what to strengthen.

## Key Features

- Accepts PRD input as markdown, pasted text, or uploaded document
- Scores against defined quality dimensions: problem clarity, outcome measurability, scope boundaries (explicit non-goals), risk identification, customer grounding, and technical feasibility acknowledgment
- Returns per-dimension scores with plain-language feedback explaining why each scored the way it did
- Provides a prioritized list of improvements — what to fix first for maximum quality lift
- Supports custom rubrics so teams can add or weight their own criteria

## Open Questions & Tradeoffs

- How opinionated should the default rubric be? A strong default POV makes it more useful out of the box but may not fit every org's style.
- Scoring model: numeric scores, letter grades, or qualitative labels (strong/needs work/missing)? Numeric feels precise but is false precision from an LLM.
- Should it suggest rewrites for weak sections, or just identify the problems? Suggestions are higher value but risk the PM outsourcing the thinking.

## Scope

Weekend build for a CLI/web tool with a fixed rubric. The scoring logic is a well-structured prompt — the real work is crafting the rubric and making the feedback actionable rather than generic.
