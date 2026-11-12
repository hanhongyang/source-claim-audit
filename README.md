# Source Claim Audit

An [Agent Skill](https://agentskills.io/specification) that audits a draft for unsourced claims, shaky numbers, inconsistent facts, and stale or mismatched citations — before you publish a research note, memo, marketplace listing, or post.

一份 Agent Skill：在发布调研、备忘、商品文案或文章之前，检查没有出处的断言、不稳的数字、前后矛盾，以及过时或不匹配的引用。

## What it does

- Inventories factual claims (numbers, comparisons, policy statements, "current" facts)
- Labels each claim as sourced, underspecified, unsourced, inconsistent, stale, or the wrong type of evidence
- Checks citations when possible, and **never invents a source to fill a gap**
- Returns a punch list with severity (`blocker` / `major` / `minor`) and a concrete fix for each issue

## Install

Copy the `source-claim-audit` folder into your agent's skills directory (for Claude Code, that is typically `.claude/skills/source-claim-audit/`), or install from this repository's root so that `SKILL.md` is at `source-claim-audit/SKILL.md`.

The skill follows the public [Agent Skills specification](https://agentskills.io/specification): a folder with a `SKILL.md` (YAML frontmatter + instructions) and optional examples.

## Use

Ask your agent to audit a draft, for example:

> Use the source-claim-audit skill on this memo. Flag anything a careful reader should not trust yet.

Or point it at a file. A worked example is in [`examples/draft-with-problems.md`](examples/draft-with-problems.md); the expected audit is in [`examples/expected-audit.md`](examples/expected-audit.md).

## License

MIT. See [LICENSE](LICENSE).
