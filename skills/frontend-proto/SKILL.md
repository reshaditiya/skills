---
name: frontend-proto
description: Use for quick, text-first frontend prototypes and small UI flows with library defaults, accessible state scaffolds, careful typography, and minimal custom styling instead of production-grade app logic.
---

# Frontend Prototyping

Use this skill for fast prototypes, small flows, forms, and early product experiments. Prioritize developer experience, clarity, and easy iteration over visual spectacle or production-grade polish. Default to a small, responsive page that makes the requested flow understandable.

## Aesthetic Goal

Default to a quiet, text-first wiki or article page. The page should feel like readable Markdown: a simple responsive one-column document where typography, a comfortable reading measure, and generous whitespace establish hierarchy. Keep the visual treatment restrained and neutral; avoid dashboard chrome, card grids, decorative containers, and marketing-heavy presentation unless the request specifically calls for them.

## Quality Bar

- Treat "prototype" as a scope and iteration constraint, not a visual excuse. Make the product-facing experience feel intentional, coherent, and finished rather than experimental, rushed, or low-effort.
- Do not expose prototype, experimental, demo, placeholder, or unfinished language in the rendered UI unless the request explicitly calls for it.
- Use complete-looking labels, states, and copy. Do not render lorem ipsum, fake claims, TODOs, or apology text as part of the product experience.

## Scope

- Implement layout, copy, controls, and visual state scaffolds by default.
- Do not implement business or application logic, API calls, authentication, persistence, data fetching, or routing unless explicitly requested. Leave a small, named local handler or stub for the user to fill in.
- Show the minimum UI needed to make the page and its states understandable. Do not add sections, controls, or chrome just to make the page feel complete.
- Preserve existing component roundedness and default styles. Do not add, remove, or tune radius values unless explicitly requested.

## Priorities

- Inspect the existing framework, package manager, UI library, state-management and validation patterns, tokens, and form patterns before coding.
- If the project is not scaffolded yet, prefer Next.js with Tailwind CSS and shadcn/ui by default.
- Reuse existing components, tokens, utilities, and default styling. Prefer defaults over custom styling, and avoid unnecessary dependencies, abstractions, and CSS.
- Keep the prototype to one page unless more is required by the flow.
- Use library-default animation only when motion is needed. Do not create custom animation timing or effects.
- Use text to explain actions and states. Do not add illustrations, images, visualizations, or icons unless explicitly required.

## Layout and Type

- Prefer a responsive one-column layout with a comfortable readable width.
- When content alone is sufficient, create only the content section; omit headers, footers, and other sections unless they are needed. Prefer a simple article/Markdown-like layout.
- Treat the page like readable markdown: one clear heading, short supporting copy, meaningful sections, and obvious actions. Prefer document flow over card grids, dashboard chrome, or decorative containers.
- Let whitespace, rather than containers, separate related sections and controls. Give the page generous, purposeful spacing without crowding it or stretching it to fill the viewport.
- Treat text as the primary visual material. Use careful copy, type size, weight, line height, spacing, and neutral shades to create hierarchy.
- Give each semantic text role a distinct level: make the page title largest and strongest, step down clearly for section headings and supporting copy, keep body text comfortable to read, and make labels, metadata, and state messages smaller and quieter without sacrificing contrast. Use size, weight, line height, spacing, and contrast together rather than relying on color alone or giving every section the same treatment.
- Keep muted text readable and avoid marketing filler, inflated claims, and placeholder-sounding copy.
- Make long text and narrow screens work without horizontal scrolling.

## Copywriting

- Keep product copy brief, plainspoken, casual, and fun. Favor relaxed "bro" energy, playful phrasing, and small jokes over formal, corporate, stiff, or overly serious language. Translate "lazy" into relaxed and effortless, never careless or unfinished.
- Prefer short sentences, specific labels, and useful microcopy. Let the interface do most of the explaining.
- Keep jokes and playful asides present when they fit. Humor must not hide the actual status, error, warning, or next step, and it should never become scolding or bleak.
- Avoid long explanations, marketing language, hype, filler, generic slogans, and placeholder copy.
- Do not call the product a prototype, experiment, demo, or work in progress in product-facing copy unless explicitly requested.

## Color and Depth

- Use existing tokens with mostly neutral colors and one restrained accent when needed.
- Use semantic colors only for errors, warnings, and success.
- Use whitespace, spacing, typography, and background shading for separation and containment. Do not use borders or drop shadows for those roles.
- Distinguish loading, empty, disabled, and inactive state UI with a muted shade or reduced opacity. Use blur only when it is already part of the default treatment and does not reduce readability. Never make color or blur the only explanation; include concise state text.
- Do not add custom borders, drop shadows, gradients, blur, or decorative color effects. Leave any treatment supplied by an existing component or library at its default.
- Give one action clear visual priority; keep secondary actions quiet.

## Forms and States

- Reuse existing state-management and validation patterns instead of introducing new dependencies.
- In React, use `useState` for simple local state. When state has multiple related fields, actions, or transitions and no existing solution is provided, use a local Flux-like `useReducer` pattern.
- Use the existing validation library when one is provided. Otherwise use native browser constraints such as `required`, `type`, `min`, `max`, and `pattern`.
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

1. Inspect the stack, reusable building blocks, and existing state-management and validation patterns.
2. Reduce the requirement to the smallest useful page, then define its copy and required states.
3. Choose the smallest appropriate state primitive: existing patterns first, then `useState` for simple React state or `useReducer` for coordinated React state.
4. Build the layout and state scaffolds with existing components, tokens, and library defaults.
5. Add only the required interactions and validation; leave unspecified behavior as stubs.
6. Check responsive behavior, text wrapping, labels, error messages, typography, spacing, and readability.

## Completion

- DX is simple: existing defaults are reused, custom code is minimal, and the implementation is easy to edit.
- The page is responsive, readable, and has purposeful breathing room.
- The UI includes only what is needed to understand the requested flow.
- Typography and copy provide the visual hierarchy through a markdown-like document flow.
- Each semantic section has a clear typographic level, with responsive sizing and readable contrast across titles, headings, body text, labels, and state copy.
- Product-facing copy is brief, casual, and fun, with a friendly bro-like voice and jokes that feel natural.
- The experience feels intentional and finished, not like a demo or unfinished experiment.
- Relevant states, labels, and field-level errors are covered.
- State UI is visibly distinct but remains readable and does not rely on color or blur alone.
- Existing roundedness and default component styling remain unchanged.
- No custom borders or drop shadows were added to contain or separate ordinary content.
- State management and validation use existing patterns or the documented primitive fallbacks.
- No production business logic, persistence, or custom animation was added without a clear request.
