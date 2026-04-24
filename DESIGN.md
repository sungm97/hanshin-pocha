```markdown
# Design System Document: The Narrative Atmosphere

## 1. Overview & Creative North Star
**Creative North Star: "The Culinary Alchemist"**

The objective of this design system is to transition from a "menu website" to a digital editorial experience. We are not just listing dishes; we are inviting guests into a dimly lit, high-end Pocha. To achieve this, the system breaks away from "The Grid" in favor of **Organic Asymmetry**. 

The design mimics the physical experience of a premium restaurant: the tactile nature of heavy paper menus, the warmth of walnut wood, and the glow of amber lighting. By utilizing overlapping elements, dramatic typographic scales, and layered depth, we ensure every scroll feels like a page turning in a high-end culinary journal.

---

## 2. Colors: Tonal Depth & Warmth
Our palette is rooted in the earth and the evening. We use rich, dark neutrals as the foundation to allow our amber and oak accents to "glow" like candlelit surfaces.

### Color Strategy
*   **Background (`#17130f`):** This is our "Dark Walnut" base. It is the canvas for all storytelling.
*   **Primary & Tertiary (`#ecc189`, `#e9c28d`):** Use these for "Illumination." They represent the warm amber glow of the interior lighting.
*   **Surface Containers:** We use `surface-container-low` (`#1f1b17`) through `highest` (`#39342f`) to define depth without lines.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to separate sections. Boundaries must be defined solely through background color shifts. For example, a featured menu item should sit in a `surface-container-high` card against a `surface` background. The shift in tone creates the edge, not a stroke.

### The "Glass & Gradient" Rule
To elevate the "premium" feel, use **Glassmorphism** for floating navigation or overlays. 
*   **Token Implementation:** Use `surface` or `surface-container` colors at 70% opacity with a `backdrop-filter: blur(20px)`. 
*   **Signature Textures:** Apply subtle linear gradients from `primary` to `primary-container` on high-level CTAs to simulate the way light hits a polished wood surface.

---

## 3. Typography: The Editorial Voice
We pair a sophisticated, high-contrast serif with a modern, clean sans-serif to create a "Heritage meets Modernity" aesthetic.

*   **Display & Headline (Newsreader):** This is our narrative voice. Use `display-lg` for hero statements and `headline-md` for section titles. These should often be center-aligned or intentionally offset from the grid to create an editorial feel.
*   **Body & Title (Manrope):** Manrope provides the "functional" contrast. Use `body-lg` for storytelling descriptions. Ensure generous line-height (1.6 or higher) to maintain the "literary" feel.
*   **Labels (Plus Jakarta Sans):** Use `label-md` in All-Caps with 10% letter spacing for metadata (e.g., "APPETIZERS" or "EST. 1988") to provide an authoritative, archival look.

---

## 4. Elevation & Depth: Tonal Layering
In this system, elevation is not about "lifting" an object away from the page, but about "stacking" layers of atmosphere.

*   **The Layering Principle:** Instead of shadows, use the surface hierarchy. Place a `surface-container-lowest` element inside a `surface-container-high` section to create "recessed" depth (like an inset alcove in a wall).
*   **Ambient Shadows:** When a floating element (like a modal or a floating action button) is required, use the following:
    *   **Blur:** 40px - 60px.
    *   **Opacity:** 6% - 8%.
    *   **Color:** Use a tinted version of `on-surface` (`#eae1da`) rather than pure black to simulate soft, ambient light dispersal.
*   **The "Ghost Border" Fallback:** If a container lacks sufficient contrast, use a **Ghost Border**: `outline-variant` (`#4f453a`) at 15% opacity. It should be felt, not seen.

---

## 5. Components: The Physical UI
Every component should feel like an object placed on a table, not a widget on a screen.

### Buttons & Interaction
*   **Primary Button:** Uses the `primary` glow (`#ecc189`). Shape: `sm` (0.125rem) or `none` (0px) for a sharp, sophisticated architectural edge. 
*   **Tertiary Button:** Use `title-sm` typography with a `primary` color bottom-border that is only 2px wide and offset by 4px of padding.
*   **Chips:** Use `surface-container-highest` with `label-md` text. No borders. These should look like small wooden tokens.

### Cards & Narrative Lists
*   **No Dividers:** Forbid the use of horizontal lines between list items. Use **Vertical White Space** (from our spacing scale) or a subtle shift from `surface-container-low` to `surface-container-lowest`.
*   **Editorial Cards:** Images should use the `md` (0.375rem) corner radius. Typography should overlap the image slightly (using negative margins) to break the "boxed-in" grid look.

### Input Fields
*   **Text Inputs:** Use a "Bottom-Line Only" approach or a very soft `surface-container` background. Error states should use `error` (`#ffb4ab`) text but maintain the soft, warm aesthetic—avoid bright "safety" reds.

---

## 6. Do's and Don'ts

### Do:
*   **Embrace Asymmetry:** Let an image sit on the left while text is offset further to the right. 
*   **Use Generous Margins:** Premium brands breathe. If you think there is enough space, add 16px more.
*   **Utilize "On-Surface-Variant":** Use this for secondary text to create a hierarchy of "light" within the page.

### Don't:
*   **No Hard Shadows:** Never use high-opacity, small-blur shadows. It breaks the "cozy lighting" illusion.
*   **No Default Grids:** Avoid the 12-column "Bootstrap" look. Think of the page as a magazine spread.
*   **No Pure White/Black:** Except for the absolute darkest points or brightest highlights, stay within our walnut and amber tokens to keep the "atmosphere" intact.

### Accessibility Note:
Ensure that while we use "soft lighting" colors, the contrast ratio between `on-surface` and `surface` always meets WCAG AA standards. Readability is the highest form of hospitality.