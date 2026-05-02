# Design System Strategy: HuddleUp

## 1. Overview & Creative North Star
This design system is built upon the Creative North Star of **"Kinetic Serenity."** 

Standard presentation decks often feel static and trapped within rigid grids. For HuddleUp, we are breaking the "template" look by introducing intentional asymmetry and editorial layering. By utilizing large-scale typography and overlapping elements (photos bleeding across containers), we create a sense of movement and professional "flow." The goal is to move beyond a simple "clean" interface into a signature digital experience that feels curated, premium, and authoritative.

## 2. Colors & Surface Philosophy
The palette is centered on a vibrant, sophisticated purple spectrum supported by a deep, ink-like neutral for readability.

### Tonal Foundations
- **Primary Power:** `primary` (#732cdb) is our signature. Use it for high-impact moments and core brand identification.
- **Surface Depth:** We utilize `surface` (#f7f6fb) as the canvas. 
- **The "No-Line" Rule:** To maintain a high-end editorial feel, designers are **strictly prohibited** from using 1px solid borders for sectioning or containment. Boundaries must be defined through:
    - **Background Color Shifts:** Placing a `surface-container-low` section against a `surface` background.
    - **Nesting:** Using `surface-container-lowest` for cards to create a soft, natural "lift."
- **Glass & Gradient Rule:** For hero sections and primary CTAs, avoid flat fills. Use a subtle linear gradient from `primary` to `primary_container`. For floating UI elements (like info badges over images), apply **Glassmorphism**: use a semi-transparent `surface_container_lowest` with a 20px backdrop-blur.

## 3. Typography
We utilize a high-contrast scale to establish an editorial rhythm.

- **Display & Headlines (Plus Jakarta Sans):** These are our "voice." Bold weights and generous tracking create a modern, confident presence. Use `display-lg` (3.5rem) for hero titles to command attention.
- **Body & Labels (Manrope):** Chosen for its technical precision and warmth. `body-lg` (1rem) is the workhorse for storytelling, while `label-md` is used for metadata and micro-copy.
- **Hierarchy Tip:** Always pair a `display` heading with a `body-md` sub-headline. The scale jump creates the "premium" feel found in high-fashion magazines and award-winning digital journals.

## 4. Elevation & Depth
In this design system, depth is a matter of layering, not decoration.

- **The Layering Principle:** Stack `surface-container` tiers (Lowest to Highest) to define importance. A card should be `surface-container-lowest` placed atop a `surface-container-low` background. This creates a tactile, "fine paper" feel.
- **Ambient Shadows:** Shadows must be felt, not seen. Use large blur values (30px-60px) and ultra-low opacity (4%-8%). Tint the shadow with `on-surface` (#2e2e33) to ensure it looks like natural ambient light rather than a digital drop shadow.
- **The "Ghost Border" Fallback:** If a layout requires a container edge for accessibility, use the **Ghost Border**: the `outline-variant` token at 15% opacity. Never use 100% opaque borders.

## 5. Components

### Buttons
- **Primary:** Filled with `primary`, text in `on-primary`. Use `rounded-full` for a friendly, modern touch.
- **Secondary:** Filled with `secondary-container`, text in `on-secondary-container`.
- **Interactions:** On hover, transition to `primary_dim`.

### Cards & Lists
- **The "No-Divider" Rule:** Forbid the use of horizontal lines to separate list items or card sections. Use vertical white space (32px+) or subtle tonal shifts between `surface-container` levels.
- **Corners:** Use `xl` (1.5rem) for main containers and `lg` (1rem) for nested elements to create a cohesive, organic silhouette.

### Input Fields
- Avoid the "box" look. Use a `surface-container-high` background with a `rounded-md` corner.
- The label should use `label-md` in `on-surface-variant`, sitting 8px above the input.

### Selection Chips
- Use `secondary-fixed` for the background with `on-secondary-fixed` for text. These should be `rounded-full` to contrast against the more structured card shapes.

## 6. Do's and Don'ts

### Do:
- **Asymmetric Overlap:** Allow images to slightly overlap the edge of a text container. It breaks the "web-template" feel.
- **Generous White Space:** If you think there is enough space, add 20% more. White space is a premium commodity.
- **Mixed Media:** Combine high-quality photography with clean, abstract illustrations using the `primary` and `secondary` purple hues.

### Don't:
- **Don't use 1px Borders:** It makes the UI feel "boxed in" and dated.
- **Don't use Pure Black:** Always use `on-surface` (#2e2e33) for text to maintain a softer, more sophisticated contrast.
- **Don't use Standard Grids:** Experiment with columns of varying widths (e.g., a 2/3 and 1/3 split) to create a more dynamic editorial layout.