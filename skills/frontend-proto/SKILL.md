---
name: frontend-proto
description: Build quick, text-first frontend prototypes with great developer experience, library defaults, markdown-like layouts, careful typography, breathing room, and minimal custom styling.
---

# Frontend Prototyping

Use this skill for fast prototypes, small flows, forms, and early product experiments. Prioritize great developer experience, clarity, and easy iteration over visual spectacle or production-grade polish.

## Priorities

- Inspect the existing framework, package manager, UI library, tokens, and form patterns before coding.
- If the project is not scaffolded yet, prefer Next.js with Tailwind CSS and shadcn/ui by default.
- Reuse existing components, tokens, utilities, and default styling. Avoid unnecessary dependencies, abstractions, and custom CSS.
- Keep the prototype to one page unless more is required. Avoid routing, persistence, and invented business logic.
- Keep handlers local and simple. If behavior is unspecified, leave a small named empty handler or stub for the user to fill in.
- Use library-default animation only when motion is needed. Do not create custom animation timing or effects.
- Use text to explain actions and states. Do not add illustrations, images, visualizations, or icons unless explicitly required.

## Layout and Type

- Prefer a responsive one-column layout with a comfortable readable width.
- When content alone is sufficient, create only the content section; omit headers, footers, and other sections unless they are needed. Prefer a simple article/Markdown-like layout.
- Treat the page like readable markdown: one clear heading, short supporting copy, meaningful sections, and obvious actions.
- Give the page breathing room with generous, purposeful spacing around sections, controls, and text. Do not crowd content or stretch it to fill the viewport.
- Treat text as the primary visual material. Use careful copy, type size, weight, line height, spacing, and neutral shades to create hierarchy.
- Keep muted text readable and avoid marketing filler, inflated claims, and placeholder-sounding copy.
- Make long text and narrow screens work without horizontal scrolling.

## Color and Depth

- Use existing tokens with mostly neutral colors and one restrained accent when needed.
- Use semantic colors only for errors, warnings, and success.
- Use subtle shadow or blur/backdrop blur only when it improves depth for a surface or overlay. Keep text surfaces clear and readable.
- Prefer shadow and blur over heavy borders, gradients, or decorative color effects.
- Give one action clear visual priority; keep secondary actions quiet.

## Forms and States

- Use the existing form and validation library. Otherwise use native browser constraints such as `required`, `type`, `min`, `max`, and `pattern`.
- Give every control an appropriate visible label. Never use placeholder text as the only label.
- Use appropriate input types, names, and autocomplete hints when useful.
- Show field-level errors, preserve entered values, and do not rely on color or a toast alone.
- Prepare relevant initial, empty, loading, submitting, disabled, success, and error states. Explain them with concise text.

## Semantics

- Use semantic HTML and real buttons and links.
- Use visible labels and native semantics first. Add `aria-label` or other ARIA only when necessary; keep it minimal so it does not clutter the code.
- Use logical headings and landmarks. Do not add custom keyboard or focus behavior when native controls are enough.

## Flow

1. Inspect the stack and reusable building blocks.
2. Reduce the requirement to the smallest useful page and write the copy and state messages.
3. Build the one-column layout with existing components, tokens, and library defaults.
4. Add only the required interactions, states, and validation.
5. Check responsive behavior, text wrapping, labels, error messages, typography, spacing, and readability.

## Completion

- DX is simple: existing defaults are reused, custom code is minimal, and the implementation is easy to edit.
- The page is responsive, readable, and has purposeful breathing room.
- Typography and copy provide the visual hierarchy.
- Relevant states, labels, and field-level errors are covered.
- Color is restrained; shadow or blur is optional and does not reduce readability.
- No custom animation or decorative visuals were added without a clear need.
