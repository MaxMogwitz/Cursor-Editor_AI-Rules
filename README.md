# CursorEditor AI Rules Documentation

## Description

This document outlines the development guidelines, code conventions, and best practices for the CursorEditor AI project. It serves as a reference to ensure consistency, maintainability, and clarity throughout the development process.

### Key Principle:
When applying rules during development or code generation, explicitly state the rule(s) being followed in the output. You may abbreviate rule descriptions to single words or short phrases as needed.

---

## Project Context
- CursorEditor AI is a TypeScript-based project focused on crafting precise and functional Chrome Extension utilities.
- It integrates advanced UI components with modern state management and scalable architecture.
- The project emphasizes modularity, security, and performance optimization.

---

## Code Style and Structure

### General Guidelines:
- **Code Style**: Write concise, modular, and functional TypeScript code with examples to clarify usage.
- **Programming Patterns**: Use functional and declarative programming; avoid class-based patterns.

### Repository Structure:
Organize files for clarity and scalability:

```
server/
├── src/
    ├── components/     # Shared React components
    ├── hooks/          # Custom React hooks
    ├── utils/          # Helper functions
    ├── types/          # TypeScript types
    └── lib/            # Shared libraries
extension/
├── src/
    ├── background/     # Service worker scripts
    ├── content/        # Content scripts
    ├── popup/          # Extension popup UI
    ├── options/        # Extension options page
    ├── components/     # Shared React components
    ├── hooks/          # Custom React hooks
    ├── utils/          # Helper functions
    ├── lib/            # Shared libraries
    ├── types/          # TypeScript types
    └── storage/        # Chrome storage utilities
shared/
├── src/
    ├── types/          # Shared TypeScript types
    └── utils/          # Shared helper functions
```

---

## Tech Stack
- **Frameworks and Libraries**: React, TypeScript, Tailwind CSS, Shadcn UI, Express.js.
- **Platforms**: Chrome Extension development with Manifest V3 standards.

---

## Naming Conventions
- **Directories**: Use lowercase with dashes (e.g., `form-wizard`).
- **Components**: Use PascalCase for files (e.g., `VisaForm.tsx`).
- **Utilities**: Use camelCase for filenames (e.g., `formValidator.ts`).
- **Exports**: Prefer named exports.

---

## TypeScript Best Practices
- Use strict typing with **interfaces** over **types**.
- Avoid **enums**; use constant objects with `as const`.
- Explicitly define return types for all functions.
- Employ discriminated unions for complex types.

---

## Chrome Extension-Specific Rules
- Adhere to Manifest V3 standards.
- Implement robust message-passing structures between components and scripts.
- Use `chrome.storage.local` for persistent state.

---

## State Management
- Leverage React Context for global states.
- Persist state using `chrome.storage`.

---

## UI and Styling
- Build UIs with Shadcn UI and Radix.
- Style components using Tailwind CSS.
- Document new Shadcn component installations.

---

## Error Handling
- Utilize error boundaries.
- Log errors for debugging while displaying user-friendly messages.
- Wrap injected scripts with error-handling mechanisms.

---

## Testing
- Focus on unit testing for utilities and components.
- Conduct E2E testing for critical user flows.
- Verify performance across multiple Chrome versions.

---

## Security
- Follow Chrome Extension security best practices.
- Sanitize inputs and enforce a strict Content Security Policy.

---

## Documentation and Workflow
- Maintain a detailed README and changelog.
- Use clear commit messages with appropriate prefixes:
  - `fix:`, `feat:`, `refactor:`, etc.
- Employ semantic versioning for releases.

