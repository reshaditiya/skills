---
name: frontend-proto
description: Use for quick, text-first frontend prototypes and small UI flows with library defaults, accessible state scaffolds, careful typography, and minimal custom styling instead of production-grade app logic.
---

# Frontend Prototyping

Use for fast prototypes, small flows, forms, and early product experiments. Prioritize clarity, easy iteration, and library defaults over visual spectacle. Default to a small, responsive page that makes the requested flow understandable.

## Principles

- Keep the product-facing experience intentional and finished. Do not expose prototype, demo, placeholder, or unfinished language; do not use lorem ipsum, fake claims, TODOs, or apology copy.
- Implement only the layout, copy, controls, and state scaffolds needed to understand the flow. Keep it to one page unless the flow requires more.
- Do not add business logic, API calls, authentication, persistence, data fetching, or routing unless explicitly requested. Leave unspecified behavior as a small, named local stub.

## Before Coding

- Inspect the framework, package manager, UI library, tokens, reusable components, state management, validation, and form patterns.
- If the project is unscaffolded, prefer Next.js with Tailwind CSS and shadcn/ui.
- Reuse existing components, tokens, utilities, and defaults. Avoid unnecessary dependencies, abstractions, and CSS. Preserve existing roundedness; do not tune radius values.

## Layout and Visuals

- Prefer a responsive, one-column article or Markdown-like layout with a readable measure, generous whitespace, one clear heading, meaningful sections, and obvious actions. Omit headers, footers, and extra chrome when content alone is enough.
- Use typography, spacing, contrast, and neutral shades to establish hierarchy. Keep muted text readable and prevent horizontal scrolling.
- Use mostly neutral existing tokens and one restrained accent. Use semantic colors only for status. Never add borders, divider lines, rules, or bordered containers to separate ordinary content; use whitespace and spacing only. Preserve borders only when they are part of an existing functional control or component default.
- Do not add custom gradients, blur, decorative effects, illustrations, images, visualizations, or icons unless explicitly required. Use library-default motion only when needed, never custom animation timing.
- Give one action clear priority; keep secondary actions quiet. Explain actions and states with text, not color alone.

## Copy

- Keep copy brief, plainspoken, casual, and fun. Use specific labels, short sentences, useful microcopy, and occasional relaxed humor.
- Avoid formal or corporate language, hype, filler, generic slogans, and jokes that obscure status, errors, warnings, or next steps. Never call the product a prototype or experiment unless requested.

## Forms, States, and Semantics

- Reuse existing state and validation patterns. Otherwise, use React `useState` for simple local state or a local `useReducer` for coordinated state; use native constraints such as `required`, `type`, `min`, `max`, and `pattern` when no validation library exists.
- Give every control a visible label; use appropriate input types, names, and autocomplete hints. Never use placeholder text as the only label.
- Cover relevant initial, empty, loading, submitting, disabled, success, and error states with concise text. Show field-level errors, preserve values, and do not rely on color or a toast alone. Distinguish inactive states without reducing readability.
- Use semantic HTML, real buttons and links, logical headings, and landmarks. Prefer native keyboard and focus behavior; add ARIA only when necessary.

## Workflow

1. Inspect the stack and existing building blocks and patterns.
2. Reduce the request to the smallest useful page, copy, interactions, and states.
3. Choose existing primitives first, then the smallest suitable local state and validation approach.
4. Build with existing components, tokens, and defaults; add only required interactions.
5. Check responsive behavior, wrapping, labels, errors, typography, spacing, contrast, and readability.

## Done When

- The page is responsive, readable, intentional, and easy to edit.
- The UI contains only what the flow needs and uses clear typographic hierarchy.
- Relevant states, labels, errors, and accessible semantics are covered.
- Existing roundedness and default styling remain intact; no decorative borders, dividers, or bordered containers were added. No unnecessary production logic, persistence, custom effects, or animation was added.
