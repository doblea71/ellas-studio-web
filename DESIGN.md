```markdown
# Design System Strategy: The Luminous Atelier

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Luminous Atelier."** 

Unlike traditional corporate "expert" brands that feel cold and clinical, this system balances authoritative mastery with the warmth of a close confidante. We move beyond the "template" look by rejecting rigid, boxy structures in favor of **Organic Editorialism**. This means using intentional asymmetry, overlapping high-fidelity imagery, and a radical commitment to "negative space" as a structural component. 

By leveraging the vibrant purples against soft, layered lilac surfaces, we create a digital environment that feels breathable, premium, and deeply personal. The layout should feel like a high-end fashion magazine transitioned into a living, breathing interface.

## 2. Color & Tonal Architecture
The palette is rooted in tonal depth rather than flat fills. We use color to guide the eye and define the "Expert Best Friend" vibe—sophisticated yet inviting.

*   **Primary Palette:** The `primary` (#7326e2) is our "expert" anchor. It should be used for high-impact moments and core CTAs.
*   **The "No-Line" Rule:** This is a core pillar of the system. **1px solid borders are strictly prohibited for sectioning.** Boundaries between content areas must be achieved through background shifts. For example, a section using `surface-container-low` (#f2effa) should transition directly into a `surface` (#f8f5ff) section.
*   **Surface Hierarchy & Nesting:** Treat the UI as physical layers of fine paper. 
    *   *Base:* `surface`
    *   *Secondary Depth:* Place a `surface-container-lowest` (#ffffff) card on top of a `surface-container-low` (#f2effa) background to create a "lifted" effect without heavy shadows.
*   **The "Glass & Gradient" Rule:** To avoid a generic look, apply a subtle linear gradient to Hero backgrounds and primary buttons (moving from `primary` to `primary-container`). For floating navigation or over-image overlays, use Glassmorphism: `surface` color at 70% opacity with a 16px-24px backdrop-blur.

## 3. Typography: The Editorial Voice
Our typography pairing is designed to be "approachable expert."

*   **Display & Headlines (Plus Jakarta Sans):** This font carries the brand’s professional weight. We use high-contrast scales (e.g., `display-lg` at 3.5rem) to create a bold, editorial feel. Headlines should use "tight" letter spacing (-0.02em) to look modern and curated.
*   **Body & Labels (Be Vietnam Pro):** This provides the "friendly" counter-balance. It is highly legible and warm. 
*   **Hierarchy as Identity:** Use `headline-lg` for value propositions, but pair them with a `label-md` "kicker" text above the headline in all-caps `primary` color to establish an authoritative, organized structure.

## 4. Elevation & Depth: Tonal Layering
We do not use structural lines. We use light and layers.

*   **The Layering Principle:** Depth is achieved by stacking the surface-container tiers. For the most premium look, nest a `surface-container-highest` element inside a `surface-container` to indicate a "pressed" or "focused" state.
*   **Ambient Shadows:** If an element must float (like a main booking button or a promo card), use a "Signature Glow." The shadow must be extra-diffused: `0px 20px 40px` with the color `on-surface` at 5% opacity. This mimics natural ambient light in a studio setting.
*   **The Ghost Border Fallback:** If a border is required for accessibility, use a "Ghost Border": the `outline-variant` token at 15% opacity. Never use 100% opaque lines.
*   **Interaction Depth:** When a user hovers over a card, do not just add a shadow; shift the background from `surface-container-low` to `surface-container-lowest`. This "inner glow" feel is more sophisticated than a standard drop shadow.

## 5. Components

### Buttons: The Kinetic Core
*   **Primary Button:** Uses the `primary` fill with `on-primary` text. Apply a `xl` (3rem) border radius to create a pill shape. 
*   **Secondary/Tertiary:** Use `secondary-container` fills. For the "Expert Best Friend" feel, tertiary buttons should be plain text with an `outline-variant` "Ghost Border" that only appears on hover.

### Cards & Collections
*   **Anti-Grid Layout:** Avoid perfectly symmetrical rows of cards. Offset the second card in a row by 40px vertically to create a dynamic, curated rhythm.
*   **No Dividers:** Use vertical white space from the `xl` (3rem) spacing scale to separate list items. Never use horizontal line rules.

### Input Fields
*   **Soft Focus:** Inputs use `surface-container-highest` backgrounds with `none` borders. On focus, the background shifts to `surface-container-lowest` and a 2px `primary` "Ghost Border" (20% opacity) appears.

### Interactive "Studio" Chips
*   **Selection Chips:** Use `secondary-fixed` for unselected and `primary` for selected. These should feel "squishy" and tactile with `md` (1.5rem) rounded corners.

## 6. Do’s and Don’ts

### Do:
*   **Do** overlap images over the edges of container backgrounds to break the "web box" feel.
*   **Do** use `display-lg` typography for short, punchy statements.
*   **Do** ensure all corners use the `lg` (2rem) or `xl` (3rem) radius to maintain the "Soft Freshness" of the brand.
*   **Do** use the logo's "eye" motif as a subtle, low-opacity background watermark in large sections to tie the brand identity into the layout.

### Don’t:
*   **Don’t** use pure black (#000000) for text. Always use `on-surface` (#2e2e35) to keep the vibe approachable.
*   **Don’t** use standard 8px or 16px margins. Embrace "Luxury Spacing"—use 64px, 80px, or 120px to let the high-end imagery breathe.
*   **Don’t** use sharp 90-degree corners. Even small elements like tooltips must have at least a `sm` (0.5rem) radius.
*   **Don’t** use "Drop Shadows" that look grey. Shadows must be a tinted lilac-grey to feel like they belong to the environment.

---
**Director's Note:** This system is not a kit of parts; it is a philosophy of light and space. Treat every screen like a gallery wall—intentional, clean, and effortlessly expert.```