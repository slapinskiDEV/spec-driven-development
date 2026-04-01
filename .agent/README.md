# .agent Workspace

Welcome to the project guidance workspace. This folder contains reusable engineering guidance, planning documents, activity logs, and project-specific documentation.

## Purpose

The `.agent` workspace is designed to provide long-term project guidance, maintain high engineering standards, and ensure historical traceability for both human developers and AI agents.

## Folder Structure

- **Core Guidance (Root):** Reusable, technology-agnostic engineering, architecture, and [testing](./testing.md) principles.
- **[plans/](./plans/):** All planning documents, organized by lifecycle stage:
  - **[plans/draft/](./plans/draft/):** Newly created plans that are not yet being executed.
  - **[plans/in-progress/](./plans/in-progress/):** Active plans that are partially completed, blocked, or awaiting user input.
  - **[plans/archived/](./plans/archived/):** Completed or retired plans (moved here **only** on explicit user instruction).
  - **[plans/template.md](./plans/template.md):** Plan template for creating new plans.
- **[Logs/](./logs/):** Historical record of project activities, decisions, and progress.
- **[Project-Specification/](./project-specification/):** Technical documentation specific to this repository.

## Plan Lifecycle

Plans follow a strict lifecycle through dedicated folders inside `plans/`:

1. **Draft** (`plans/draft/`) — A new plan starts here. It is a proposal under review, not yet being executed.
2. **In Progress** (`plans/in-progress/`) — Once work begins and the plan is not fully completed, move it here. Keep it here while tasks are pending, blocked, or require user action.
3. **Archived** (`plans/archived/`) — A plan may only be moved here when the **user explicitly instructs** the agent to archive it. The agent must **never** archive plans on its own.

### Plan Content Requirements

Every plan file must include an execution tracking section that clearly shows:

- Which items were **completed**
- Which items are **pending**
- Which items are **in-progress**
- Which items are **blocked**
- Which items **require user action**

Use a status table or checklist so progress is easy to scan. Once execution starts, the plan must reflect implementation progress — it is not only a static proposal.

### Important Restrictions

- Do **not** archive plans automatically.
- Do **not** assume a completed plan should be moved to archived.
- Do **not** hide unfinished work.
- Do **not** leave plan progress undocumented.
- Do **not** treat blocked items as completed.
- Do **not** create a plan without execution tracking.

## Operating Model & Workflow

To maintain project quality and consistency, follow this workflow:

1. **Read Core Guidance:** Familiarize yourself with the engineering, architecture, and [testing](./testing.md) principles in the root of `.agent/`.
2. **Plan Major Changes:** For any significant feature or refactor, create a new plan in `plans/draft/` using the [template](./plans/template.md).
3. **Review & Refine:** Review the plan to ensure it aligns with project principles. Refine as necessary.
4. **Approve & Implement:** Once a plan is solid, proceed with implementation. Move the plan to `plans/in-progress/`.
5. **Track Progress:** Update the plan's execution status as tasks are completed, blocked, or require user input.
6. **Record Activity:** Log your progress, decisions, and any deviations from the plan in `logs/`.
7. **Maintain Documentation:** Keep the `project-specification/` area up to date as the project evolves.
8. **Update Tasks & Decisions:** Use `tasks.md` and `decisions.md` to track ongoing work and key architectural choices.
9. **Archive Only on User Request:** When the user explicitly says to archive a plan, move it to `plans/archived/`.

## Logging Rule

Logging is centralized in a single file: [`logs/changelog.md`](./logs/changelog.md).

At the end of each completed task or meaningful change, append a short entry to the changelog. Do not create separate log files for individual tasks, sessions, or plan events unless explicitly requested. The changelog serves as a lightweight project memory for fast context recovery in future sessions. See [logs/README.md](./logs/README.md) for details.

## Definition of Done (Mandatory)

> **Hard rule: no task is complete until `.agent/logs/changelog.md` is updated.**

Every completed task must end with these steps, in order:

1. Update the relevant files.
2. Update task or plan status if needed.
3. Append an entry to `logs/changelog.md`.

The changelog entry is **not optional**. If it is missing, the work is incomplete. See [`definition-of-done.md`](./definition-of-done.md) for full details.
