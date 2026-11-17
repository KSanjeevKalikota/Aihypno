# Aihypno

This repository holds a working-method playbook for Claude Code, packaged as a skill. It tells the model how to approach any task: understand the request, plan the steps, execute, check its own work before claiming it is done, and report the result faithfully.

There is no application code here. The repository consists of the playbook and the instruction that loads it.

## What's in the repository

| Path | Purpose |
|---|---|
| [`.claude/skills/fable-playbook/SKILL.md`](.claude/skills/fable-playbook/SKILL.md) | The playbook itself, as a Claude Code skill named `fable-playbook`. |
| [`CLAUDE.md`](CLAUDE.md) | Project instructions that tell Claude to load the skill at the start of every task. |
| `README.md` | This file. |

## What the playbook covers

1. **Before you start:** state the goal, separate what was asked from what is assumed, define what "done" looks like, read before writing, and record the starting state.
2. **Planning:** resolve the riskiest unknown first, split the work into steps that can each be verified, keep the change small, and set a scope boundary.
3. **Executing:** verify after each step, debug from evidence, fix causes rather than symptoms, and take care with anything hard to undo.
4. **Before you say it is done:** reread the request, run the proof, review your own diff, test edge cases, and confirm the work was delivered.
5. **Reporting:** lead with the outcome, report failures plainly, and separate what was verified from what was not.
6. **Mistakes to watch for:** a table of tempting thoughts, what each one really means, and what to do instead.

Read [`SKILL.md`](.claude/skills/fable-playbook/SKILL.md) for the full text.

## How to use it

1. Start a Claude Code session in this repository.
2. Claude Code discovers the skill in `.claude/skills/` and lists it as `fable-playbook`.
3. `CLAUDE.md` tells Claude to load the skill at the start of every task, so no extra step is needed.
4. To load the skill on demand, ask Claude to use the `fable-playbook` skill, or type `/fable-playbook`.

To change how Claude works in this repository, edit `SKILL.md`.
