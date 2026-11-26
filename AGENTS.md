# <repo-name>

<One line: what this repo is and who uses it.>

## Shared context

Polinom.io rules are synced into `.ai/` and edited centrally, not here; `project-overview.md` and `business-rules.md` are owned by this repo and never overwritten by the sync. Load them lazily:

- `.ai/global.md`: always loaded; read it first if your harness has not.
- `.ai/engineering/engineering.md`: always loaded; read it first if your harness has not.
- `.ai/project-overview.md`: before planning, scoping or explaining work in this repo.
- `.ai/business-rules.md`: before changing domain logic, data models or validations.
- `.ai/engineering/tech-stacks/tech-stacks.md`, then the stack files present in that folder: before writing or reviewing code.
- `.ai/company-public.md`: before describing Polinom.io publicly.

## Commands

Defaults for Node (pnpm); replace per stack.

- Install: `pnpm install --frozen-lockfile`
- Test: `pnpm test`
- Lint: `pnpm lint`

## Architecture

<3–10 lines: main folders and what calls what.>

## Rules

<Only what differs from the company defaults.>
