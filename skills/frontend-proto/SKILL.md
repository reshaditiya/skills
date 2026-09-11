---
name: frontend-proto
description: Use for quick, text-first frontend prototypes and small UI flows with library defaults, accessible state scaffolds, careful typography, and minimal custom styling instead of production-grade app logic.
---

# Frontend Prototyping

Use this skill for fast prototypes, small flows, forms, and early product experiments. Prioritize developer experience, clarity, and easy iteration over visual spectacle or production-grade polish. Default to a small, responsive page that makes the requested flow understandable.

## Scope

- Implement layout, copy, controls, and visual state scaffolds by default.
- Do not implement business or application logic, API calls, authentication, persistence, data fetching, or routing unless explicitly requested. Leave a small, named local handler or stub for the user to fill in.
- Show the minimum UI needed to make the page and its states understandable. Do not add sections, controls, or chrome just to make the page feel complete.

## Priorities

- Inspect the existing framework, package manager, UI library, tokens, and form patterns before coding.
- If the project is not scaffolded yet, prefer Next.js with Tailwind CSS and shadcn/ui by default.
- Reuse existing components, tokens, utilities, and default styling. Avoid unnecessary dependencies, abstractions, and custom CSS.
- Keep the prototype to one page unless more is required by the flow.
- Use library-default animation only when motion is needed. Do not create custom animation timing or effects.
- Use text to explain actions and states. Do not add illustrations, images, visualizations, or icons unless explicitly required.

## Layout and Type

- Prefer a responsive one-column layout with a comfortable readable width.
- When content alone is sufficient, create only the content section; omit headers, footers, and other sections unless they are needed. Prefer a simple article/Markdown-like layout.
- Treat the page like readable markdown: one clear heading, short supporting copy, meaningful sections, and obvious actions.
- Let whitespace, rather than containers, separate related sections and controls. Give the page generous, purposeful spacing without crowding it or stretching it to fill the viewport.
- Treat text as the primary visual material. Use careful copy, type size, weight, line height, spacing, and neutral shades to create hierarchy.
- Keep muted text readable and avoid marketing filler, inflated claims, and placeholder-sounding copy.
- Make long text and narrow screens work without horizontal scrolling.

## Color and Depth

- Use existing tokens with mostly neutral colors and one restrained accent when needed.
- Use semantic colors only for errors, warnings, and success.
- Use whitespace, spacing, typography, and background shading for separation and containment. Do not use borders or drop shadows for those roles.
- Distinguish loading, empty, disabled, and inactive state UI with a muted shade, reduced opacity, or restrained blur. Never make color or blur the only explanation; include concise state text.
- Use a restrained shadow only when an overlay such as a dialog or popover needs elevation. Keep ordinary text surfaces clear and readable.
- Avoid gradients and decorative color effects.
- Give one action clear visual priority; keep secondary actions quiet.

## Forms and States

- Use the existing form and validation library. Otherwise use native browser constraints such as `required`, `type`, `min`, `max`, and `pattern`.
- Give every control an appropriate visible label. Never use placeholder text as the only label.
- Use appropriate input types, names, and autocomplete hints when useful.
- Show field-level errors, preserve entered values, and do not rely on color or a toast alone.
- Prepare relevant initial, empty, loading, submitting, disabled, success, and error states. Explain them with concise text.
- Keep unspecified submission and data behavior as a local stub rather than inventing an implementation.

## Semantics

- Use semantic HTML and real buttons and links.
- Use visible labels and native semantics first. Add `aria-label` or other ARIA only when necessary; keep it minimal so it does not clutter the code.
- Use logical headings and landmarks. Do not add custom keyboard or focus behavior when native controls are enough.

## Flow

1. Inspect the stack and reusable building blocks.
2. Reduce the requirement to the smallest useful page, then define its copy and required states.
3. Build the layout and state scaffolds with existing components, tokens, and library defaults.
4. Add only the required interactions and native validation; leave unspecified behavior as stubs.
5. Check responsive behavior, text wrapping, labels, error messages, typography, spacing, and readability.

## Completion

- DX is simple: existing defaults are reused, custom code is minimal, and the implementation is easy to edit.
- The page is responsive, readable, and has purposeful breathing room.
- The UI includes only what is needed to understand the requested flow.
- Typography and copy provide the visual hierarchy.
- Relevant states, labels, and field-level errors are covered.
- State UI is visibly distinct but remains readable and does not rely on color or blur alone.
- No borders or drop shadows are used to contain or separate ordinary content.
- No production business logic, persistence, or custom animation was added without a clear request.
