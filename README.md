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

Copy this repository folder into your Codex skills directory, or upload the folder/zip to a skill platform that supports `SKILL.md`.

The skill entrypoint is:

```text
SKILL.md
```

## Suggested Prompt

```text
Use $bid-response-production to review my tender file, proposal draft, scoring table, screenshots, and workload sheet. Produce formal Chinese technical bid materials with clear commitments, assumptions, evidence, formatting checks, and unresolved questions.
```

## Contents

```text
SKILL.md
agents/openai.yaml
references/format-baseline.md
references/risk-checklist.md
```

## License

MIT
