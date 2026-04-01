# Logs Area

This folder contains the project's historical activity log.

## Purpose

Logging is centralized in a single file: [`changelog.md`](./changelog.md).

The changelog is a lightweight project memory. It is updated at the end of completed work to help the agent (or developer) quickly recover project context when returning later.

## Mandatory Rule

> **Hard rule: no task is complete until `changelog.md` is updated.**

Updating the changelog is the **final step** of every completed task. If the entry is missing, the work is incomplete. This is not optional documentation — it is part of task completion. See [`../definition-of-done.md`](../definition-of-done.md).

## Rules

- Use `changelog.md` as the **default and primary** log — do not create separate log files for tasks, sessions, or plan events unless explicitly requested.
- Write to the changelog only **after** a task or meaningful change is completed.
- Keep entries short, clear, and easy to scan.
- Use a simple chronological format (newest first).
- Do not turn the changelog into long-form documentation.
- Do not log every micro-step — only summarize completed work.
- Do **not** skip the changelog.
- Do **not** postpone the changelog.
- Do **not** treat changelog updates as optional.

## What the Changelog Should Help Answer

- What was done recently?
- What areas were changed?
- What was added, updated, or fixed?
- What should the agent quickly know when returning to the project?

## Legacy Templates

The `template.md` file in this folder is retained for reference but is **not the default** logging method. The default is to append entries directly to `changelog.md`.
