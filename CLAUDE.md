# Personal Organizer — instructions for Claude

This repo is the owner's personal organizer. The owner chats with Claude regularly;
Claude keeps these files up to date. **The files are the source of truth** — always
read the relevant file before answering or editing, and commit + push after every change.

## Layout
| Path | What lives there |
|---|---|
| `inbox.md` | Quick captures not yet sorted. Triage into the right file when asked (or when obvious). |
| `tasks.md` | Personal to-do list, grouped by priority/section. |
| `shopping.md` | Shopping list, grouped by store/category. |
| `projects/<slug>.md` | One file per personal project (copy `projects/_template.md`). `projects/README.md` is the index. |
| `notes/<slug>.md` | Standalone notes, ideas, reference info. `notes/README.md` is the index. |
| `journal/YYYY-MM.md` | Dated log of what was discussed/decided, newest entry at top. |
| `archive/` | Completed tasks, bought items, finished projects (`archive/YYYY.md` for tasks/shopping). |

## Conventions
- Checkboxes: `- [ ] item` open, `- [x] item` done. Optional tags at end: `(due: YYYY-MM-DD)`, `#tag`, `!high`.
- When something is done/bought, tick it; on a "clean up" request move ticked items to `archive/YYYY.md` with the completion date.
- Dates are ISO (`YYYY-MM-DD`). Keep `Last updated:` lines current.
- New project → copy `_template.md`, add a line to `projects/README.md`. Same for notes.
- Add a short journal entry for any meaningful session (decisions, new projects, big changes).
- Commit messages: short and descriptive, e.g. `tasks: add renew passport`, `shopping: tick milk, eggs`.
- Never put passwords, account numbers, or other secrets in this repo.

## Artifacts
When the owner asks for a view (dashboard, list, checklist), build it from these files and
publish it as an artifact. Record artifact links in `artifacts.md` so they can be reused/updated
instead of creating new ones each time.

## Common requests
- "Add X to my list" → `tasks.md` (or `shopping.md` if it's something to buy).
- "Remind me / note that…" → `inbox.md` or the matching note/project.
- "What's on my plate?" → summarize open items in `tasks.md` + active projects' next steps.
