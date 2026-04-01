# Clean Code Guidelines

The goal of clean code is readability and maintainability. These rules should be applied throughout the project.

## Core Rules

- **Readability Over Cleverness:** Write code that is easy to read and understand, even for someone unfamiliar with the project.
- **Clear and Descriptive Naming:** Choose names that accurately reflect the purpose and responsibility of variables, functions, and classes.
- **Single Responsibility Principle (SRP):** Each unit of code (function, class, module) should do one thing and do it well.
- **Small and Focused Units:** Keep functions and classes small. If a unit of work is too large, break it down into smaller pieces.
- **Minimize Side Effects:** Functions should be predictable and have minimal unexpected consequences outside their scope.
- **Avoid Duplication (DRY):** Don't repeat code. If you find yourself copying and pasting, consider refactoring into a reusable component.
- **Meaningful Documentation:** Whenever you create a new function or significantly rewrite an existing one, add an English documentation comment above it using the `/** ... */` syntax.
- **Function Comment Responsibility:** The comment must briefly explain what the function does, focus on purpose and behavior, and be concise and useful. Do not write generic or meaningless comments.
- **English Language for Documentation:** Always use English for these comments.
- **Documentation Style:** Use `/** ... */` style for function comments consistently across the project.
- **Self-Documenting Code First:** While functions must have the `/** ... */` documentation, the code itself should still be as self-documenting as possible through clear and descriptive naming.
- **Comments Explain 'Why' and 'What':** Outside of function documentation, comments should primarily explain *why* something is done, rather than *how* (which should be clear from the code).
- **Keep it Simple:** Avoid unnecessary abstractions and complexity. Start simple and evolve as needed.
