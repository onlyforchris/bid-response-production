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

## Install Automatically

Ask Codex or another agent that supports Codex skills to install it for you:

```text
Please install the Codex skill from GitHub repository onlyforchris/bid-response-production.
Use the skill path skills/bid-response-production.
After installing, tell me whether I need to restart Codex.
```

If the agent has the built-in `$skill-installer`, this prompt is enough:

```text
$skill-installer install from onlyforchris/bid-response-production path skills/bid-response-production
```

Equivalent installer command:

```bash
python ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py --repo onlyforchris/bid-response-production --path skills/bid-response-production
```

On Windows, the script path is usually:

```bash
python %USERPROFILE%\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py --repo onlyforchris/bid-response-production --path skills/bid-response-production
```

Restart Codex if the skill does not appear immediately.

## Install Manually

Clone this repository:

```bash
git clone https://github.com/onlyforchris/bid-response-production.git
```

Then copy this folder:

```text
skills/bid-response-production
```

into one of your Codex skill locations.

Common user-level locations:

```text
macOS/Linux: ~/.agents/skills/bid-response-production
Windows: %USERPROFILE%\.agents\skills\bid-response-production
```

Repo-level location:

```text
<your-repo>/.agents/skills/bid-response-production
```

Restart Codex after copying if the skill does not appear.

## Use

Invoke it explicitly:

```text
$bid-response-production
```

Suggested working prompt:

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
