# Workflow Guidance

This document describes the workflow for making changes to the project.

## Standard Workflow

1.  **Understand the Problem:** Thoroughly investigate the issue or requirement before starting any work.
2.  **Review Core Guidance:** Ensure that your intended change aligns with the engineering and architecture principles in the root of `.agent/`.
3.  **Plan Major Changes:** For significant features, refactors, or architectural changes, create a new plan in `plans/draft/` using the [template](./plans/template.md).
4.  **Review the Plan:** Review and refine the plan to ensure it meets project standards and requirements.
5.  **Begin Implementation:** Move the plan to `plans/in-progress/` and start working. Update the plan's execution status as you go.
6.  **Create and Update Tests:** For new functionality, bug fixes, or changed behavior, ensure appropriate test coverage is included, following the [testing principles](./testing.md).
7.  **Log Progress:** After completing a task or meaningful change, append a short entry to `logs/changelog.md`.
8.  **Update Task List:** Maintain `tasks.md` to keep track of current and future work.
9.  **Document Decisions:** Record key architectural or technical choices in `decisions.md`.
10. **Maintain Specification:** Keep the `project-specification/` documentation accurate as the repository evolves.

## Plan Lifecycle

Plans follow a strict folder-based lifecycle inside the `plans/` directory:

### 1. Draft (`plans/draft/`)

- All newly created plans go here.
- A draft plan is a proposal under review — it may be edited, discussed, or rejected.
- No implementation work has started yet.

### 2. In Progress (`plans/in-progress/`)

Move a plan here when:
- Execution has started.
- Some tasks were completed but others remain.
- Some tasks are blocked or require user intervention.
- The plan cannot be fully completed in the current state.

While in progress, the plan must be kept up to date with execution status for every task.

### 3. Archived (`plans/archived/`)

- A plan may only be moved here when the **user explicitly instructs** the agent to archive it.
- **The agent must never archive plans on its own.**
- Completed plans should remain in `plans/in-progress/` until the user decides to archive them.

### Plan Content Requirements

Every plan must include an execution tracking section (table or checklist) that clearly shows the status of each task:

- **completed** — work is done
- **pending** — not yet started
- **in-progress** — currently being worked on
- **blocked** — cannot proceed due to a dependency or issue
- **requires-user-action** — needs user input, approval, credentials, or manual intervention

This tracking must be explicit and easy to scan. The plan is not only a static proposal — once execution starts, it must reflect implementation progress.

### Important Restrictions

- Do **not** archive plans automatically.
- Do **not** assume a completed plan should be moved to archived.
- Do **not** hide unfinished work.
- Do **not** leave plan progress undocumented.
- Do **not** treat blocked items as completed.
- Do **not** create a plan without execution tracking.

## When to Plan

A plan is required for:

- New features
- Large refactors
- Architectural changes
- Cross-cutting improvements
- Integrations
- Work affecting multiple modules or areas

## When to Log

Logging is centralized in a single file: `logs/changelog.md`. The system is intentionally simple.

- Write to the changelog only **after** a task or meaningful change is completed.
- Keep entries short, clear, and easy to scan.
- Use a simple chronological format.
- Do **not** create separate log files for individual tasks, sessions, or plan events.
- Do **not** log every micro-step — only summarize completed work.

The changelog serves as a lightweight project memory. It should help answer:
- What was done recently?
- What areas were changed?
- What was added, updated, or fixed?
- What should the agent quickly know when returning to the project?

## Definition of Done

> **Hard rule: no task is complete until `.agent/logs/changelog.md` is updated.**

Every completed task must end with these final steps, in order:

1. Update the relevant files.
2. Update task or plan status if needed.
3. Append an entry to `logs/changelog.md`.

**The changelog entry is mandatory.** If it is missing, the work is incomplete.

- Do **not** skip the changelog.
- Do **not** postpone the changelog.
- Do **not** treat changelog updates as optional documentation.
- Do **not** finish a task without updating `logs/changelog.md`.

See [`definition-of-done.md`](./definition-of-done.md) for full details.
