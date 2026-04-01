# Testing Principles

Testing is a first-class citizen in this project. It provides confidence, prevents regressions, and serves as documentation for expected behavior.

## Core Principles

- **Confidence over Coverage:** Focus on tests that provide real confidence that the system works as intended. High coverage is less valuable than high-quality, reliable tests.
- **Regression Prevention:** Every bug fix should, whenever possible, include a regression test to ensure the issue does not reappear.
- **Readable and Reliable:** Tests should be easy to read and understand. Avoid complex logic in tests. Flaky tests should be fixed or removed.
- **Reflect Real Behavior:** Tests should verify outcomes and behavior, not implementation details. This makes refactoring easier.
- **Balance:** Use a mix of unit, integration, and higher-level tests to balance speed, isolation, and confidence.

## Test Categories

- **Unit Tests:** Focus on individual components, functions, or classes in isolation. These should be fast and frequent.
- **Integration Tests:** Verify that multiple units work together correctly. These catch issues in the boundaries between components.
- **Higher-Level Tests (E2E/UI):** Validate end-to-end workflows from the user's perspective. These provide the highest confidence but are typically slower and more complex.

## When to Create or Update Tests

- **New Functionality:** Include appropriate tests for new features to define and verify their behavior.
- **Bug Fixes:** Add a test that reproduces the bug before fixing it, ensuring the fix is effective and permanent.
- **Changed Behavior:** When existing behavior is intentionally modified, review and update the corresponding tests to reflect the new requirements.
- **Refactoring:** Use existing tests to ensure that internal changes do not break existing functionality. Add tests if coverage is missing before starting the refactor.

## Quality Attributes

- **Fast:** Tests should run quickly to provide rapid feedback.
- **Isolated:** Tests should not depend on each other or external state that can't be easily controlled.
- **Repeatable:** Tests should produce the same result every time they are run in the same environment.
- **Self-Validating:** Tests must clearly pass or fail without requiring manual inspection of logs or output.
