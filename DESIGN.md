# Design System: Editorial Serenity

## 1. Overview & Creative North Star

### Creative North Star: "The Modern Cloister"
This design system is a digital translation of the monastic experience—quiet, intentional, and deeply grounded. It moves away from the frenetic, edge-to-edge nature of the modern web in favor of a **contained, single-column editorial flow**. By utilizing a centered layout with generous margins, we create a sanctuary for the user's attention.

The visual language rejects "standard" UI tropes like heavy borders and generic grids. Instead, it relies on **tonal depth and sophisticated typography** to guide the eye. We favor asymmetry in image placement and overlapping elements to provide a custom, high-end feel that reflects the unique architectural heritage of a pilgrimage house.

---

## 2. Colors

The palette is rooted in the earth (Terracotta) and light (Cream), designed to feel warm and inviting rather than sterile.

### Tonal Strategy
*   **Primary (`#914529`)**: Reserved for moments of high importance—signature CTAs, hero accents, and brand markers.
*   **Secondary/Tertiary (`#805345`, `#6e573b`)**: Used to create warmth in supporting elements and decorative icons.
*   **Surface Tiers**: The depth of the interface is built on the `surface` tokens. We move from `surface-container-low` (for subtle sectioning) to `surface-container-highest` (for elevated focus areas).

### The "No-Line" Rule
**Explicit Instruction:** 1px solid borders are strictly prohibited for defining sections. Boundaries must be defined solely through background color shifts. To separate content, transition from `surface` to `surface-container-low` or `surface-variant`. This creates a seamless, premium feel that avoids the "boxed-in" look of cheaper templates.

### Glass & Gradient Signature
To elevate the experience, floating elements (like a navigation bar or a sticky reservation bar) should utilize **Glassmorphism**. Use a semi-transparent `surface` color with a `backdrop-filter: blur(12px)`. For main CTAs, apply a subtle linear gradient from `primary` to `primary-container` to give the button "soul" and a tactile, three-dimensional quality.

---

## 3. Typography

The typography scale is the primary driver of the brand's authoritative yet welcoming voice.

*   **Display & Headlines (`newsreader`)**: A sophisticated serif. Use `display-lg` (3.5rem) for hero moments to evoke the feeling of a prestige travel journal. The tight tracking and intentional line height convey tradition and history.
*   **Body & Titles (`workSans`)**: A clean, modern sans-serif. This provides the "Modern" half of the brand's "Traditional yet Modern" promise. It ensures maximum legibility for long-form descriptions of the house's history and room details.
*   **Labeling**: Use `label-md` in all-caps with a 0.05rem letter-spacing for category headers to create an organized, curated hierarchy.

---

## 4. Elevation & Depth

In this system, depth is organic, not structural.

*   **The Layering Principle**: Instead of shadows, stack surface tiers. A card using `surface-container-lowest` placed on a background of `surface-container-low` creates a soft, natural lift.
*   **Ambient Shadows**: When physical elevation is required (e.g., a modal or floating booking widget), shadows must be extra-diffused. 
    *   *Blur:* 24px–40px. 
    *   *Opacity:* 4%–6%. 
    *   *Color:* Use a tinted `on-surface` (warm brown) rather than black to mimic natural light filtered through a window.
*   **The Ghost Border**: If accessibility requires a stroke (e.g., in input fields), use `outline-variant` at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons
*   **Primary**: Gradient-filled (`primary` to `primary-container`), `md` roundedness (0.375rem). Text should be `title-sm` in `on-primary`.
*   **Secondary**: `surface-container-highest` background with `on-surface` text. No border.
*   **Tertiary**: Text-only using `primary` color, with a 2px underline that appears on hover.

### Cards & Content Blocks
*   **Constraint**: Forbid the use of divider lines. 
*   **Separation**: Use vertical white space (Spacing `12` or `16`) or subtle background shifts. 
*   **Asymmetry**: Images in cards should slightly bleed outside the container or overlap with text blocks to break the "grid" feel.

### Input Fields
*   **Style**: Use `surface-container-lowest` for the field background. 
*   **Focus State**: Transition the "Ghost Border" from 15% to 60% opacity using the `primary` color. Avoid heavy glow effects.

### Navigation
*   **The Floating Header**: A glassmorphic bar (`surface` at 80% opacity + blur) that sits at the top of the contained column, not the full width of the browser.

---

## 6. Do's and Don'ts

### Do
*   **Do** use the single-column flow to guide the user through a narrative journey.
*   **Do** allow images to have different aspect ratios (e.g., a tall portrait image next to a wide landscape block) to create an editorial layout.
*   **Do** use `Spacing 20` (7rem) between major sections to let the design breathe.

### Don't
*   **Don't** use 100% black (`#000000`) for text; always use `on-surface` (`#1e1b15`) to maintain the warmth of the palette.
*   **Don't** use full-width sections. Keep all content within a max-width container (e.g., 1100px) to maintain the "pilgrimage house" intimacy.
*   **Don't** use sharp `none` corners. Always apply at least `sm` or `md` roundedness to maintain the "Soft Minimalism" aesthetic.