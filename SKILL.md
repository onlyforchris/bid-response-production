---
name: bid-response-production
description: Produce and review Chinese technical bid materials, including technical proposals, response matrices, screenshots and figures, workload estimates, team/resume appendices, DOCX/PPT/XLSX deliverables, formatting normalization, and final compliance checks.
---

# Bid Response Production

## Principle

Treat every deliverable as a formal technical bid, not an essay or demo note. Ground claims in the latest tender file, clarification notes, customer template, current system evidence, and verifiable delivery boundaries.

## Source Priority

1. Tender file, scoring table, customer template, clarification or addendum.
2. Current system, source code, product documentation, verified screenshots, and project records.
3. Existing proposal draft.
4. Historical bid samples.

Historical samples may provide structure and phrasing ideas, but do not inherit project-specific commitments, customer names, old system boundaries, fonts, or line spacing.

## Workflow

1. Identify the source-of-truth files:
   - tender file and scoring table
   - clarification/addendum
   - current proposal draft
   - screenshots, architecture diagrams, or runnable product
   - workload, quotation, staffing, and resume appendices
2. Classify the task:
   - full rewrite: scope or architecture is wrong, outdated, or demo-like
   - local edit: one section, person, table, attachment, or wording issue
   - evidence pack: screenshots, diagrams, captions, and proof text
   - response matrix: point-by-point tender compliance
   - workload estimate: effort table fill or reasonableness check
   - final QA: claims, tone, style, attachments, and formatting
3. Build or update a compact compliance map:
   - tender requirement
   - response section
   - evidence or screenshot
   - commitment boundary
   - assumptions and unresolved questions
4. Draft or revise content:
   - use formal Chinese bid style
   - separate commitments, assumptions, customer dependencies, and items requiring later verification
   - preserve tender terms when they are scoring-table terms
   - replace demo language with delivery, validation, or evidence language
5. Verify before claiming done:
   - DOCX: inspect paragraphs and table cells
   - XLSX: inspect changed cells and formulas
   - screenshots: visually inspect final images
   - final package: list deliverables and unresolved blockers

## Writing Rules

- Prefer formal party references such as `我司/贵司` unless the target document already has an approved convention.
- Do not make unconditional claims about availability, accuracy, concurrency, automation, recognition rate, or system responsibility.
- Tie metrics to test conditions, data scope, acceptance method, and responsibility boundary.
- Screenshots must prove a bid point. Add concise captions explaining what each screenshot demonstrates.
- Do not use `POC`, `演示`, `测试数据`, `Excel`, debug labels, localhost URLs, TODO markers, or temporary wording in final bid-facing content.
- If changing a named person's role or resume wording, synchronize the main bid document and any standalone resume attachment.

## Default Formatting

Use the customer template or tender requirement first. If neither specifies formatting, use the baseline in `references/format-baseline.md`.

Hard defaults:
- body text: SimSun/宋体, 小四, black
- table text: SimSun/宋体, 小四, black
- body and table line spacing: 1.5
- historical FangSong/仿宋 body text, 12 pt body text, and 1.0 table line spacing are issues to normalize, not options to preserve

## References

- Use `references/format-baseline.md` when creating or normalizing DOCX layout.
- Use `references/risk-checklist.md` before final delivery or when reviewing historical bid samples.

## Output Patterns

### Technical Proposal

Deliver:
- rewritten section or document
- concise change summary
- commitment/assumption/verification notes

### Response Matrix

Columns:
- tender requirement
- response position
- evidence/material
- compliance level
- assumptions or risk
- owner or next action

### Screenshot/Figure Pack

Deliver:
- cleaned screenshots or diagrams
- captions mapped to tender requirements
- missing-evidence list

### Workload Estimate

Deliver:
- edited workbook or effort table
- formula cells verified
- reasonableness judgment against formal delivery scope

## Red Flags

- The text sounds like a generic AI essay.
- The proposal promises a metric without test conditions.
- Screenshots show demo/internal/debug labels.
- Old customer names, project names, dates, or system boundaries remain.
- A DOCX review only checked paragraphs while key content is in tables.
- Historical formatting overrides the required style baseline.
