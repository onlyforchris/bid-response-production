# Bid Response Production

A Codex skill for producing and reviewing Chinese technical bid materials.

It helps with:

- technical proposal rewrites
- response matrices
- screenshot and figure evidence packs
- workload estimate checks
- DOCX/PPT/XLSX compliance review
- bid formatting normalization
- risk-word cleanup before final delivery

## Install

Use Codex's skill installer:

```bash
python ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py --repo onlyforchris/bid-response-production --path skills/bid-response-production
```

Or copy this folder into a Codex skills directory:

```text
skills/bid-response-production
```

Restart Codex if the skill does not appear immediately.

## Suggested Prompt

```text
Use $bid-response-production to review my tender file, proposal draft, scoring table, screenshots, and workload sheet. Produce formal Chinese technical bid materials with clear commitments, assumptions, evidence, formatting checks, and unresolved questions.
```

## Contents

```text
skills/bid-response-production/SKILL.md
skills/bid-response-production/agents/openai.yaml
skills/bid-response-production/references/format-baseline.md
skills/bid-response-production/references/risk-checklist.md
```

## License

MIT
