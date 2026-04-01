# Definition of Done

A task, plan execution, or meaningful change is **not complete** until all of the following are satisfied:

## Checklist

1. **Code / file changes are applied** — all relevant files have been updated.
2. **Plan status is updated** (if applicable) — the plan's execution tracking reflects the current state of every task.
3. **Changelog is updated** — a short entry has been appended to [`logs/changelog.md`](./logs/changelog.md).

## Mandatory Changelog Rule

> **Hard rule: no task is complete until `.agent/logs/changelog.md` is updated.**

- The changelog entry is the **final step** of every completed task.
- If the changelog entry is missing, the work is **incomplete**.
- Do **not** skip the changelog.
- Do **not** postpone the changelog.
- Do **not** treat changelog updates as optional documentation.
- Do **not** finish a task without updating `logs/changelog.md`.

## What Must Be Logged

Each changelog entry must include:

- **Date**
- **What was done**
- **What was added, changed, updated, or fixed**
- Optionally: which plan, area, or module it relates to

Keep entries short and practical.

## Enforcement

Your final steps for every completed task must be, in order:

1. Update the relevant files.
2. Update task or plan status if needed.
3. Append an entry to `logs/changelog.md`.

Only after step 3 may you treat the work as finished.
