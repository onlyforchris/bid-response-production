# Risk Checklist

Run this before delivering a technical bid or before reusing a historical sample.

## Source Risks

- Latest tender file, scoring table, and clarification were not checked.
- Existing proposal draft is treated as truth instead of secondary material.
- Historical customer names, project names, product names, dates, or system boundaries remain.

## Bid Tone Risks

- Generic essay tone or marketing filler.
- The first chapter starts with broad industry or policy background before explaining the specific project response.
- The project positioning or `我司对本项目的核心理解` section is thin and does not state response strategy, differentiators, delivery boundary, and evidence plan.
- Claims are broad but not tied to implementation evidence.
- The text does not separate commitments, assumptions, customer dependencies, and items requiring verification.

## Structure Risks

- Functional modules do not follow the minimum pattern: 功能实现, 技术要点, 业务联动, 差异化能力, 验收/证据口径.
- A full technical proposal was drafted without first creating a top-level directory/outline.
- The outline has no chapter-level page budget, so the agent cannot tell whether it is drafting a 120+ page bid or a thin technical-plan skeleton.
- No tender directory exists, but the proposal does not follow or adapt the baseline in `technical-proposal-outline.md`.
- The proposal is far below a 120+ page DOCX-equivalent plan when there is no tender page cap or user request for a brief.
- Macro background, policy background, or industry trends exceed about 20% of the first chapter.
- A scoring item has response text but no evidence chapter, screenshot, table, test condition, or acceptance method.
- A module claims to answer from four or five dimensions, but the actual subheadings only cover function, technical points, or business linkage.
- Banking, treasury, finance, or controlled business modules omit permission, audit, security, approval, or exception-control wording.

## Risk Words To Search

Clean or justify:

- `POC`
- `演示`
- `测试数据`
- `模拟数据`
- `debug`
- `localhost`
- `127.0.0.1`
- `TODO`
- `TBD`
- `临时`
- `占位`
- `截图待补`
- `待完善`
- `[投标人名称]`
- `[客户名称]`
- `[项目名称]`
- `[日期]`
- `XX`
- `某某`
- `待填`
- `年月日`

Also search for bracket placeholders with a pattern such as `[.*]`.

Review `Excel` by context:

- Keep legitimate product capabilities such as Excel import/export templates when they are part of the tendered function.
- Rewrite manual Excel ledgers, Excel as the primary control mechanism, or temporary Excel workarounds into controlled batch import, system integration, data validation, or governance language.

Review strong commitments:

- `确保`
- `保证`
- `全面`
- `完全`
- `100%`
- `无误`
- `零风险`
- `自动完成`
- `无需人工`

For each strong commitment, require statistical scope, period/trigger, exceptions, and acceptance method.

Review weak commitments:

- `可根据`
- `可支持`
- `原则上`
- `尽量`
- `力争`
- `视情况`
- `可能`
- `或可`

## Evidence Risks

- Screenshot has no caption or does not map to a scoring item.
- Screenshot shows internal labels, demo data, debug state, or empty pages.
- Architecture diagram is decorative but does not explain scope, integration, security, or workflow.

## Formatting Risks

- Body is not 宋体小四.
- Table text is not 宋体小四.
- Table line spacing is 1.0 instead of 1.5.
- Historical 仿宋 or 12 pt body style leaked into the final document.
- Figure/table captions are missing or inconsistent.
