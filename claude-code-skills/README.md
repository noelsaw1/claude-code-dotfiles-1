# Claude Code Skills for AWS — Reusable Slash Commands

![Claude Code](https://img.shields.io/badge/Claude_Code-5C4EE5?logo=anthropic&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonwebservices&logoColor=white)
![draw.io](https://img.shields.io/badge/draw.io-F08705?logo=diagramsdotnet&logoColor=white)

Reusable [Claude Code skills](https://docs.anthropic.com/en/docs/claude-code/slash-commands) (formerly called slash commands) for AWS workflows. Each skill is a `.md` file with instructions that Claude loads automatically or on demand via `/skill-name`.

> These skills follow the open [SKILL.md standard](https://docs.anthropic.com/en/docs/claude-code/slash-commands), which works across Claude Code, GitHub Copilot, Cursor, and other AI coding tools that support skill files.

---

## Available Skills

| Skill | Description | Invoke with |
|-------|-------------|-------------|
| [aws-architecture-diagram-generator](./aws-architecture-diagram-generator.md) | Generates professional AWS architecture diagrams in draw.io (`.drawio`) format with official AWS4 icons, color-coded data flows, region containers, and animated edges | `/drawio` |

---

## How to Install a Skill

### Option 1 — Copy to your Claude Code skills directory

```bash
# New skills directory (recommended)
mkdir -p ~/.claude/skills
cp claude-code-skills/aws-architecture-diagram-generator.md ~/.claude/skills/drawio/SKILL.md

# Or legacy commands directory (still works)
cp claude-code-skills/aws-architecture-diagram-generator.md ~/.claude/commands/drawio.md
```

The skill becomes available as `/drawio` in your next Claude Code session.

### Option 2 — If you cloned this repo as `~/.claude`

The skills are already in place. No extra steps needed.

---

## How to Create Your Own Skills

1. Create a folder in `~/.claude/skills/` with a `SKILL.md` file inside
2. Add YAML frontmatter with `name` and `description` (Claude uses the description to decide when to auto-load the skill)
3. Write the prompt body with instructions

```markdown
---
name: my-skill
description: When to use this skill and what it does
---

Your instructions here.
```

You can also use the legacy format: a `.md` file directly in `~/.claude/commands/`. The filename becomes the slash command name (`drawio.md` -> `/drawio`).

See the [official Claude Code skills docs](https://docs.anthropic.com/en/docs/claude-code/slash-commands) for the full reference.

---

## Contributing

Contributions are welcome! See [CONTRIBUTING](../CONTRIBUTING.md) for more information.

---

## Security

If you discover a potential security issue in this project, notify AWS/Amazon Security via the [vulnerability reporting page](http://aws.amazon.com/security/vulnerability-reporting/). Please do **not** create a public GitHub issue.

---

## License

This library is licensed under the MIT-0 License. See the [LICENSE](../LICENSE) file for details.
