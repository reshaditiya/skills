---
name: frontend-proto
description: Build quick, text-first frontend prototypes with a library-first approach, compact one-column layouts, careful copy, restrained color, and minimal custom styling.
---

# Frontend Prototyping

Use this skill for fast frontend prototypes, small flows, forms, and early product experiments. Optimize for speed, clarity, readable text, and easy iteration rather than visual spectacle or production-grade polish.

## Working Rules

- Inspect the project before coding. Identify the framework, package manager, existing UI/component library, form and validation libraries, design tokens, and local conventions.
- Reuse existing components, tokens, utilities, and patterns. Do not add a dependency when the project already provides a solution.
- Prefer library primitives and layout utilities over custom CSS. Add custom styling only when the library cannot express a required layout or interaction.
- Keep one-off prototype code local and simple. Extract components only when they are reused or the split makes the code easier to understand.
- Keep the prototype to one page unless the requirement explicitly needs more. Do not add routing, persistence, animations, or abstractions that are not needed to demonstrate the flow.
- Prefer text over illustrations, images, and icons. Explain actions and state changes with short, clear writing.

## Layout

- Default to a single-column layout so the page stays readable and responsive.
- Use multiple columns only when the requirement clearly needs separation. Never add columns just to fill available space.
- Use a comfortable max width and leave breathing room around content. Do not stretch every section to the full viewport width unless the requirement calls for it.
- Treat the page like readable markdown: one clear heading, short supporting copy, meaningful sections, and obvious actions.
- Keep the structure compact. Avoid dashboards, dense grids, decorative hero sections, and extra panels unless the user asks for them.
- Ensure the layout works on narrow screens, with longer text, and without horizontal scrolling.

## Text and Visual Hierarchy

- Treat text as the primary visual material. Write copy that is plain, direct, concise, and carefully edited.
- Use clear headings, labels, helper text, and state messages. Give each section one clear job.
- Use type size, weight, line height, spacing, and restrained neutral shades to distinguish headings, body text, supporting text, metadata, and status messages.
- Keep softer text readable. Do not use low contrast just to create hierarchy.
- Avoid marketing jargon, inflated claims, and placeholder-sounding prose.
- Prefer labels such as "Add task", "Save changes", or "Nothing here yet" over promotional language.
- Do not add illustrations, images, visualizations, or icons unless explicitly required.
- Do not invent brand language, metrics, testimonials, or product claims.

## Color and Actions

- Use mostly neutral backgrounds, text, borders, and surfaces with one restrained accent hue when needed.
- Use the existing design tokens when available.
- Create hierarchy with text shade, weight, size, and spacing rather than decorative color.
- Use semantic colors only for errors, warnings, and success; these are status states, not extra branding colors.
- Give one action clear visual priority. Keep secondary actions quiet, using text or a basic outline instead of competing filled buttons.
- Avoid gradients, decorative color effects, and styling that makes non-actions look clickable.

## Forms and Validation

- Inspect existing dependencies and project patterns before implementing a form.
- Use the existing form and validation library when one is already present.
- If no library exists, use native browser validation with semantic controls and constraints such as `required`, `type`, `min`, `max`, and `pattern`. Use the Constraint Validation API only when native constraints are not enough.
- Associate every control with an appropriate visible label. Never use placeholder text as the only label. Use `fieldset` and `legend` for related controls when appropriate.
- Use appropriate input types, names, and autocomplete hints when they improve the form.
- Show useful, field-level errors near the relevant control. Do not rely on color, a toast, or a single generic message.
- Preserve entered values after validation failures and make the invalid state easy to find.
- Do not build a custom validation system for a simple prototype when browser validation is sufficient.

## State Coverage and Behavior

- Prepare the useful states for each main flow: initial, empty, loading, submitting, disabled, success, and error.
- Explain states with concise text. Do not add an illustration, image, or icon to compensate for unclear copy.
- Keep event handlers and business logic local, simple, and easy to replace.
- If behavior or an API is not provided, use a small named empty handler or simple stub for the user to fill in. Do not invent persistence, network behavior, or complex business rules.

## Accessibility and Semantics

- Use semantic elements such as `header`, `nav`, `main`, `section`, `form`, `label`, `button`, `fieldset`, `legend`, `ul`, and `ol` according to their meaning.
- Keep semantics separate from presentation. Use the UI library's styling props, classes, or tokens for appearance, and use the correct semantic element or `as`/`component` option for meaning.
- Prefer a real `button` or link over a clickable `div`.
- Use a logical heading hierarchy and clear landmarks.
- Use visible labels and native semantics first. Add `aria-label` or other ARIA only when native HTML cannot provide the necessary accessible name or relationship.
- Keep ARIA minimal. Do not use it to compensate for incorrect HTML or add it to every control by default.
- Do not add custom keyboard or focus behavior unless the required interaction cannot work with native controls.

## Implementation Flow

1. Inspect the existing stack and reusable building blocks.
2. Reduce the requirement to the smallest useful page and content structure.
3. Write the page copy and state messages before adding decorative styling.
4. Build the semantic one-column layout with existing components and tokens.
5. Add only the interactions, state coverage, and validation needed to demonstrate the flow.
6. Check narrow-screen behavior, text wrapping, labels, validation messages, state messages, and text hierarchy.

## Completion Checklist

Before considering the prototype complete, confirm:

- The page is one column unless a two-column layout is clearly useful.
- The page has comfortable spacing, a readable width, and no horizontal scrolling.
- Existing libraries and tokens were reused.
- Custom CSS and new dependencies are justified.
- The copy is direct, carefully written, and free of marketing filler.
- Text hierarchy is clear through typography, spacing, and restrained neutral shades.
- Empty, loading, submitting, disabled, success, and error states are covered where relevant.
- Forms use an existing validation library or native browser validation.
- Every form control has an appropriate visible label and useful error feedback.
- ARIA is used only when native semantics are not enough.
- Event handlers and business logic are minimal, with unspecified behavior left as simple stubs.
- The page uses mostly neutral colors and no decorative illustrations, images, or icons unless required.
- Only the primary CTA is visually prominent; other actions are quieter.
