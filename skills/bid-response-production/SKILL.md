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
3. For a full technical proposal, build the top-level outline first.
   - Follow the tender/customer required directory when provided.
   - If no directory is provided, use `references/technical-proposal-outline.md`.
   - Plan for 120+ pages unless the tender sets a shorter page limit. Do not pad; allocate enough depth to requirements, modules, evidence, implementation, service, risk, and appendices.
   - Include a page-budget table by chapter before drafting. If the draft is materially below the page budget, call it an outline or first pass, not a complete technical bid.
   - Put requirement response, scoring response, evidence, and appendix chapters into the outline from the start; do not leave them as afterthoughts.
4. Build or update a compact compliance map:
   - tender requirement
   - response section
   - evidence or screenshot
   - commitment boundary
   - assumptions and unresolved questions
5. Draft or revise content:
   - use formal Chinese bid style
   - separate commitments, assumptions, customer dependencies, and items requiring later verification
   - preserve tender terms when they are scoring-table terms
   - replace demo language with delivery, validation, or evidence language
   - make the opening bid-specific before expanding into general background
6. For DOCX output from a Markdown draft, use `scripts/md_to_bid_docx.py` instead of hand-building one-off Word formatting code. Then review the result with `scripts/review_bid_docx.py`.
7. Verify before claiming done:
   - DOCX: inspect paragraphs and table cells
   - XLSX: inspect changed cells and formulas
   - screenshots: visually inspect final images
   - final package: list deliverables and unresolved blockers

## Writing Rules

- Prefer formal party references such as `我司/贵司` unless the target document already has an approved convention.
- Do not make unconditional claims about availability, accuracy, concurrency, automation, recognition rate, or system responsibility.
- Tie metrics to test conditions, data scope, acceptance method, and responsibility boundary.
- Screenshots must prove a bid point. Add concise captions explaining what each screenshot demonstrates.
- Do not use `POC`, `演示`, `测试数据`, debug labels, localhost URLs, TODO markers, or temporary wording in final bid-facing content.
- Treat `Excel` by context: legitimate import/export templates may remain as product capability; manual Excel ledgers, temporary Excel workarounds, or Excel as the primary delivery mechanism must be rewritten as controlled batch import, system integration, or data governance language.
- If changing a named person's role or resume wording, synchronize the main bid document and any standalone resume attachment.

## Opening Section Rules

For full technical proposals, do not start the main body with generic industry background. Before broad background, write a bid-specific opening section of about 800-1200 Chinese characters that covers:

- project positioning in one sentence
- customer scenario and pain points
- our response strategy and delivery boundary
- three to five core differentiators
- evidence plan: which chapters, screenshots, tables, or modules prove the response

Limit macro background, policy background, and industry trends to supporting material. As a rule of thumb, generic background should stay below 20% of the first chapter, and each paragraph must explain why it matters to this project.

The first chapter should not bury `我司对本项目的核心理解` at the end as a short summary. Put the project response summary, response strategy, and evidence path before industry background, or make them section 1.1.

## Full Proposal Scale

When the user asks for a complete technical bid, do not produce a thin first draft. Unless the tender specifies a page cap or the user asks for a brief, target a 120+ page DOCX-equivalent plan. Use content depth, not filler:

- first chapter: bid-specific understanding, response strategy, pain points, value, key success factors
- architecture chapters: business, application, data, integration, deployment, security, performance
- function chapters: every required module or scoring item with the full module response pattern
- evidence chapters: screenshots, diagrams, response tables, acceptance evidence
- delivery chapters: implementation, testing, migration, training, operations, SLA, risk, emergency plan
- appendices: team, resumes, qualifications, deliverables, deviation table, glossary

The first step is the top-level directory/outline. Use the tender directory first; otherwise use `references/technical-proposal-outline.md` as the baseline and tailor it to the project.

For a Markdown first draft, still enforce DOCX-equivalent depth. A 40,000-character draft with 30+ modules is usually only an outline or first pass, not a complete 120+ page bid. Major functional modules should normally contain 800-1200+ Chinese characters each; minor interface or service items should normally contain 400-800+ Chinese characters each. If evidence is not available, add an explicit evidence-needed note in the compliance map instead of omitting the evidence path.

## Full Proposal Generation Loop

For a complete DOCX technical bid, do not try to finish the whole document in one generation pass. Use this loop:

1. Build outline, page budget, and compliance map.
2. Draft chapter 1 and the response matrix first.
3. Expand functional modules in batches of 5-8 modules.
4. After each batch, check module depth before continuing.
5. Convert to DOCX only after the Markdown content passes the depth gate.
6. Run `scripts/review_bid_docx.py` and fix the reported issues.

Depth gate:

- core modules: 800-1200+ Chinese characters each
- ordinary modules: 500-800+ Chinese characters each
- minor interface/service items: 300-500+ Chinese characters each
- every module must include function, business flow, technical mechanism, permission/audit/security control, exceptions, linkage, and acceptance/evidence

If the module average is below 700 Chinese characters or any module is below 300 Chinese characters, do not proceed to final DOCX delivery. Expand the thin modules first.

## Module Response Pattern

For each functional module or scoring item, use this minimum structure unless the tender template requires otherwise:

1. 功能实现: concrete user-facing capabilities and operating flow.
2. 技术要点: architecture, integration, data, security, performance, or implementation mechanism.
3. 业务联动: upstream/downstream modules, data flow, approval flow, or external systems.
4. 差异化能力: why this response is stronger than a generic implementation.
5. 验收/证据口径: screenshots, reports, logs, test conditions, or acceptance evidence.

If a section only lists functions without technical points, business linkage, and evidence, treat it as unfinished.

Do not say a module is written from "four dimensions" or "five dimensions" unless those dimensions are present as actual subheadings or clearly separated paragraphs. For banking, treasury, finance, and controlled business systems, add permission/audit/security controls to each major module unless the tender explicitly excludes them.

## Claim Boundaries

When using absolute or numeric commitments such as `100%`, `确保`, `保证`, `无误`, or `自动完成`, attach:

- statistical scope
- time period or trigger condition
- exception handling
- acceptance or verification method

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
- Use `references/technical-proposal-outline.md` when the tender does not provide a required directory.

## Output Patterns

### Technical Proposal

Deliver:
- rewritten section or document
- concise change summary
- commitment/assumption/verification notes
- first-chapter strength check: whether the opening is bid-specific enough
- outline/page-depth check: whether the planned technical proposal is broad enough for a 120+ page formal bid when no shorter limit is given

For a natural-language request such as "generate a DOCX technical bid from this tender", use this minimum path:

1. Extract or summarize tender requirements and scoring items.
2. Draft the technical proposal in Markdown using the required tender directory or `references/technical-proposal-outline.md`.
3. Convert Markdown to DOCX:
   `python scripts/md_to_bid_docx.py draft.md 技术标书.docx --title "项目名称" --bidder "投标人名称" --date "日期"`
4. Run:
   `python scripts/review_bid_docx.py 技术标书.docx`
5. Fix placeholder, risk-word, structure, and formatting issues before delivery.

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
- The first chapter opens with generic industry/policy background and delays the project-specific response.
- `我司对本项目的核心理解` or equivalent positioning section is only a short summary instead of a full bid-specific response.
- The proposal promises a metric without test conditions.
- Functional modules omit technical points, business linkage, differentiators, or evidence.
- Screenshots show demo/internal/debug labels.
- Old customer names, project names, dates, or system boundaries remain.
- Placeholder fields remain in the final document.
- A DOCX review only checked paragraphs while key content is in tables.
- Historical formatting overrides the required style baseline.

## Scope Limits

This skill supports bid writing, review, normalization, and evidence planning. It does not replace legal, commercial, security, compliance, or customer-side review. If tender terms, pricing, liability, personal data, regulated security controls, or contractual commitments are involved, flag the item for owner confirmation instead of silently turning it into a commitment.
