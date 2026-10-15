# skills

Claude Code のスキル置き場です。スキルの本文は日本語で書いています。

| スキル | 内容 |
| --- | --- |
| [design-security-check](design-security-check/SKILL.md) | 設計書・API 設計・PR を7つの問いで簡易にセキュリティチェックする。「セキュアじゃない」と「コストを考えると過剰」の両方を指摘する |
| [model-suggest](model-suggest/SKILL.md) | タスクの不確実性から、Claude のモデルと effort の組み合わせを助言する |
| [tidy-context](tidy-context/SKILL.md) | CLAUDE.md・rules・スキルの指示を「ルールか情報源か」「いつでも要るか、特定のフォルダ・作業のときだけか」で仕分け、置き場所を提案する |

## 使い方

使いたいスキルのフォルダを、プロジェクトの `.claude/skills/` か、全プロジェクトで使うなら `~/.claude/skills/` にコピーするか、シンボリックリンクを張ります。

```sh
ln -s "$(pwd)/tidy-context" ~/.claude/skills/tidy-context
```

## English

Skills for Claude Code. The skill files are written in Japanese; Claude follows them when you talk to it in English too.

| Skill | What it does |
| --- | --- |
| [design-security-check](design-security-check/SKILL.md) | A quick security check of a design doc, API design or PR, using seven questions. It points out both what is not secure enough and what costs more than the risk is worth |
| [model-suggest](model-suggest/SKILL.md) | Suggests a Claude model and effort level based on how uncertain the task is |
| [tidy-context](tidy-context/SKILL.md) | Sorts each instruction in CLAUDE.md, rules and skills by two questions: is it a rule or a fact, and is it needed always or only for one folder or task? Then it proposes where each one should live. For stale or conflicting instructions, use `/doctor prompt-audit` |

### Install

Copy or symlink a skill folder into your project's `.claude/skills/`, or into `~/.claude/skills/` to use it in every project.

```sh
ln -s "$(pwd)/tidy-context" ~/.claude/skills/tidy-context
```
