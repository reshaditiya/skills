---
name: legacy-modernize
description: Use when modifying, debugging, or gradually modernizing a legacy or poorly maintained application. Preserve existing conventions inside legacy code, follow applicable AGENTS.md guidance for new code, and prefer small reversible changes.
---

# Legacy Modernization

Modernize legacy applications incrementally without turning every task into a rewrite. Preserve working behavior and project knowledge first; introduce better patterns at safe boundaries.

## Priorities

When guidance conflicts, use this order:

1. The user's requested behavior and safety of the change.
2. Applicable repository instructions, especially `AGENTS.md`.
3. Existing project contracts, utilities, components, dependencies, and runtime support.
4. Modern patterns that are compatible with the project's installed versions.
5. General preferences or new abstractions.

Do not let generic best practices override repository-specific instructions or existing behavior without a concrete reason.

## Before Coding

- Find and read every applicable `AGENTS.md` from the repository or workspace root through the target directory. Read relevant `README`, `CONTRIBUTING`, and project documentation as well.
- Inspect the package manifest, lockfile, runtime and framework versions, scripts, build configuration, and test configuration before choosing an implementation pattern.
- Inspect the target file, its callers, exports, data contracts, nearby tests, and neighboring components. Search for existing utilities and patterns before creating anything new.
- Classify the change as an edit to legacy code, genuinely new code, or a boundary between both. Use that classification to choose conventions.
- Establish a baseline with the narrowest relevant test, lint, typecheck, build, or manual verification command when behavior is uncertain.

## Editing Existing Legacy Code

- Preserve the local module style, naming, exports, APIs, data formats, error behavior, supported runtime, and dependency choices unless the request requires changing them.
- Keep the diff focused. Do not reformat files, rename unrelated symbols, upgrade frameworks, or perform drive-by cleanup.
- When new behavior must be added to an old file, integrate it with the smallest compatible change. Extract a new module only when it creates a clear seam or improves safety.
- Do not force strict typing, a new state model, a new component system, or a new architecture onto an entire legacy area as part of a focused task.

## Writing New Code

- Read the applicable `AGENTS.md` instructions and follow the project's current patterns before writing a new file or feature.
- Use modern, idiomatic APIs that are supported by the installed framework, language, runtime, and browser targets. Do not upgrade dependencies just to use a newer pattern.
- Reuse existing utilities, components, design tokens, validation, state management, data access, error handling, test helpers, and scripts before introducing replacements.
- If no local pattern exists, choose the smallest maintainable pattern that fits the existing stack. Check the relevant versioned documentation when using a framework, library, SDK, or platform API.
- Keep new code isolated from legacy details where practical. Translate at the boundary instead of spreading legacy assumptions through the new code.

## Incremental Migration

- Prefer one behavior or boundary at a time over a big-bang rewrite.
- Add characterization tests when existing behavior is unclear and the behavior matters to the change.
- Separate behavior changes from mechanical refactors so failures are easy to diagnose.
- Use adapters, facades, or small compatibility layers when they make a migration reversible and do not duplicate existing utilities.
- Migrate one caller or path, verify it, then continue. Remove old code only after searching for usages and verifying runtime behavior.
- Avoid changing persistence formats, public APIs, authentication, deployment configuration, or other hard-to-reverse contracts without explicit need and a migration or rollback path.

## Developer Experience

- Search before inventing. Prefer one familiar project utility over a new helper that solves the same problem slightly differently.
- Use the repository's existing scripts and commands. Do not introduce custom tooling when the project already has an equivalent workflow.
- Keep changes easy to review: small files, narrow diffs, clear names, and no unrelated formatting.
- Avoid new dependencies unless an existing project capability cannot meet the requirement. Check installed versions before proposing one.
- Preserve useful error messages, loading states, and local development workflows while modernizing implementation details.
- If instructions, behavior, or ownership are unclear, state the uncertainty and ask before making a risky architectural decision.

## Image-Based UI Requests

- Treat the image as a low-fidelity product reference, not a final visual specification. Prioritize the requested flow, content hierarchy, semantics, and responsive behavior over pixel-perfect matching.
- Default to creating a new local component for the requested screen or prototype.
- Reuse an existing component only when its behavior already matches the requirement or reuse clearly avoids duplication without distorting the prototype.
- Even in a new component, reuse existing primitives, utilities, tokens, accessibility patterns, and project conventions.
- Do not modify a shared component solely to match one image or one prototype screen.

## Verification

- Run the narrowest relevant tests first, followed by the project's existing lint, typecheck, build, or integration checks when applicable.
- For UI changes, check responsive behavior, keyboard and focus behavior, labels, empty/loading/error/success states, and existing consumers of changed shared components.
- Review the final diff for accidental formatting, unrelated cleanup, dependency changes, contract changes, and leaked legacy assumptions.
- If a check cannot run, explain why and state what was verified instead.

## Done When

- The requested behavior works without an unnecessary rewrite.
- Existing legacy behavior and contracts are preserved unless an intentional change was requested.
- New code follows applicable repository guidance and uses compatible modern patterns.
- Existing utilities and components were reused where appropriate.
- The migration boundary is clear, the diff is focused, and relevant verification was completed.
