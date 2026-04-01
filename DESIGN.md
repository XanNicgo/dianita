# Design System: The Digital Keepsake

## 1. Overview & Creative North Star
**Creative North Star: "The Modern Heirloom"**

This design system moves away from the "transactional" feel of e-commerce to create an experience that feels like opening a handwritten letter or a curated scrapbooked memory. We reject the rigid, boxy constraints of standard web design in favor of **Organic Elegance**. 

To achieve this, the system utilizes intentional asymmetry—placing elements slightly off-center to mimic the human touch—and heavy utilization of "Negative Space as a Feature." We aren't just selling gifts; we are framing emotions. The interface should feel like a series of layered, high-end stationery papers floating in a soft, ethereal light.

---

## 2. Colors & Surface Philosophy
The palette is rooted in sophisticated blushes and deep berries, moving beyond "baby pink" into a romantic, editorial territory.

### The "No-Line" Rule
**Explicit Instruction:** You are prohibited from using 1px solid borders to define sections. 
*   **The Technique:** Transitions must be handled via background shifts. For instance, a Hero section using `surface` (`#fef8f9`) should transition into a featured gift section using `surface-container-low` (`#f8f2f3`). This creates a "soft-edge" transition that feels premium and seamless.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of fine paper. 
*   **Lowest Layer:** `surface` or `surface-bright` for the main canvas.
*   **Secondary Layer:** Use `surface-container` (`#f3ecee`) for large content blocks.
*   **Action Layer:** Use `surface-container-lowest` (`#ffffff`) for interactive cards to make them appear "lifted" by light rather than shadows.

### The "Glass & Gradient" Rule
To add "soul," use subtle gradients for primary CTAs and header accents.
*   **Signature Gradient:** Linear 135° from `primary` (`#ac2d5e`) to `primary-container` (`#fd6c9c`).
*   **Glassmorphism:** For mobile navigation bars or floating "Add to Cart" prompts, use `surface` at 80% opacity with a `20px` backdrop-blur. This allows the romantic imagery of the site to bleed through the UI, maintaining an emotional connection.

---

## 3. Typography: The Editorial Voice
The system relies on a high-contrast pairing between the structural **Epilogue** and the approachable **Plus Jakarta Sans**.

*   **Display & Headline (Epilogue):** These are your "Handwritten" moments. Use `display-lg` for hero statements. To achieve the "script" feel requested, apply a custom `font-style: italic` and tight letter-spacing to these tokens. They represent the "Heartbeat" of the brand.
*   **Body & Labels (Plus Jakarta Sans):** These provide the "Modern" balance. They must remain clean and highly legible. 
*   **Hierarchy Tip:** Never use `headline-sm` and `body-lg` at the same visual weight. Force a contrast; if the headline is `primary`, the body should be `on-surface-variant` to ensure the "Editorial" feel isn't lost in a sea of uniform text.

---

## 4. Elevation & Depth
We eschew the "Material 2" style of heavy shadows. We define depth through **Tonal Layering**.

*   **The Layering Principle:** Place a card using `surface-container-lowest` on a background of `surface-container-high`. The 4% difference in luminance is enough for the eye to perceive a boundary without a harsh line.
*   **Ambient Shadows:** If a shadow is required for a floating "Gift Selection" modal, use: `box-shadow: 0 20px 40px rgba(172, 45, 94, 0.06)`. Note the use of the `primary` color in the shadow—this "Ambient Glow" feels more natural and romantic than a grey shadow.
*   **The "Ghost Border" Fallback:** For input fields, use `outline-variant` at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons (The "Soft-Touch" Action)
*   **Primary:** Gradient of `primary` to `primary-container`. `Roundedness: full`. High-elevation ambient shadow on hover.
*   **Secondary:** `surface-container-highest` background with `primary` text. No border.
*   **Tertiary:** `primary` text, no background, `italic` Epilogue font to mimic a handwritten signature.

### Cards & Lists (The "Unbound" Style)
*   **Rule:** Forbid divider lines (`<hr>`). 
*   **Execution:** Separate list items using `spacing-6` (2rem) of vertical white space or a subtle toggle between `surface` and `surface-container-low` backgrounds.
*   **Roundedness:** Use `lg` (2rem) for product cards and `xl` (3rem) for image containers to maintain a soft, organic feel.

### Input Fields (The "Letter" Input)
*   Floating labels using `label-md`. 
*   Background: `surface-container-lowest`. 
*   Bottom-only "Ghost Border" to mimic the lines on a notepad.

### Signature Component: "The Memory Carousel"
A mobile-first horizontal scroll component where images use `rounded-xl` and slightly overlap. Use `spacing-2` as the negative margin between overlapping images to create a "scattered photos" aesthetic.

---

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical margins. For example, a heading might have a `spacing-8` left margin but a `spacing-12` right margin.
*   **Do** use `primary-fixed-dim` for "Save for Later" icons to provide a muted, emotional warmth.
*   **Do** leverage the `surface-tint` to give a very slight pinkish hue to all transparent overlays.

### Don't
*   **Don't** use pure black (`#000000`) for text. Use `on-surface` (`#353134`) to keep the contrast "soft-romantic" rather than "high-contrast tech."
*   **Don't** use `rounded-none`. In this system, sharpness is the enemy of emotion. Even the smallest elements should use at least `rounded-sm`.
*   **Don't** stack more than three levels of surface containers. It breaks the "flat-paper" metaphor and begins to look cluttered.

---

## 7. Spacing Rhythm
The spacing scale is built on a `0.35rem` (approx 5.6px) base to ensure a non-standard, bespoke rhythm.
*   **Section Padding:** Always use `spacing-16` or `spacing-20` for top/bottom padding. This design system breathes; do not crowd the "Modern Heirloom."
*   **Micro-interactions:** Use `spacing-1.5` for the gap between an icon and its label.