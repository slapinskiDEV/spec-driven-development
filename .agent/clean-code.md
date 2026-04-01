# Clean Code Guidelines

The goal of clean code is readability and maintainability. These rules should be applied throughout the project.

## Core Rules

- **Readability Over Cleverness:** Write code that is easy to read and understand, even for someone unfamiliar with the project.
- **Clear and Descriptive Naming:** Choose names that accurately reflect the purpose and responsibility of variables, functions, and classes.
- **Single Responsibility Principle (SRP):** Each unit of code (function, class, module) should do one thing and do it well.
- **Small and Focused Units:** Keep functions and classes small. If a unit of work is too large, break it down into smaller pieces.
- **Minimize Side Effects:** Functions should be predictable and have minimal unexpected consequences outside their scope.
- **Avoid Duplication (DRY):** Don't repeat code. If you find yourself copying and pasting, consider refactoring into a reusable component.
- **Meaningful Structure:** Organize code in a logical and consistent way.
- **Clear Error Handling:** Handle errors explicitly and provide meaningful context. Avoid silent failures.
- **Consistency in Style and Patterns:** Follow the existing coding style and established patterns within the repository.
- **Explicit over Implicit:** Prefer explicit code that is easy to follow over clever or implicit behavior.
- **Comments as a Last Resort:** Comments should explain *why*, not *what*. Code should be self-documenting whenever possible.
- **Keep it Simple:** Avoid unnecessary abstractions and complexity. Start simple and evolve as needed.
