# Design System Document

## 1. Overview & Creative North Star: "The Artisanal Curator"

This design system moves away from the sterile, "bootstrap" aesthetic common in administrative tools. Instead, it adopts the persona of **The Artisanal Curator**. Much like a high-end coffee tasting room, the interface is designed to feel spacious, tactile, and intentional. 

The "Creative North Star" is **Organic Editorialism**. We break the rigid, boxy grid of standard dashboards by using intentional white space, sophisticated tonal layering, and high-contrast typography scales. The goal is to make the management of "THE KING OF COFFEE" feel less like data entry and more like curating a premium brand experience. We prioritize depth through color shifts rather than lines, ensuring a "soft-touch" professional finish.

---

## 2. Colors: Tonal Depth & The "No-Line" Rule

The palette is rooted in the rich, earthy tones of specialty coffee, balanced by the "Steam" neutrals of a clean café environment.

### The "No-Line" Rule
**Strict Mandate:** Designers are prohibited from using 1px solid borders to section off content. Structural boundaries must be defined solely through background color shifts or subtle tonal transitions. 
- Use `surface-container-low` for secondary sections sitting on a `surface` background.
- Use `surface-container-lowest` (#FFFFFF) for primary content cards to create a natural "lift."

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like fine paper stacked on a wooden counter.
- **Base Layer:** `surface` (#F8F9FA) – The foundation.
- **Mid Layer:** `surface-container` (#EDEEEF) – For grouped content or sidebar backgrounds.
- **Top Layer:** `surface-container-lowest` (#FFFFFF) – For interactive cards and focal points.

### The "Glass & Gradient" Rule
To elevate the "King" status of the brand, use Glassmorphism for floating overlays (e.g., Modals or Profile Dropdowns). Apply `surface` at 80% opacity with a `20px` backdrop blur. For primary CTAs, use a subtle linear gradient from `primary` (#553722) to `primary_container` (#6F4E37) at a 135-degree angle to add "visual soul."

---

## 3. Typography: The Editorial Voice

We utilize **Be Vietnam Pro** for its exceptional Vietnamese character support and its clean, professional geometric rhythm.

| Scale | Token | Size | Weight | Role |
| :--- | :--- | :--- | :--- | :--- |
| **Display** | `display-lg` | 3.5rem | 700 | High-impact metrics (e.g., Daily Revenue). |
| **Headline** | `headline-md` | 1.75rem | 600 | Section titles (e.g., Inventory Management). |
| **Title** | `title-md` | 1.125rem | 500 | Card headers and modal titles. |
| **Body** | `body-md` | 0.875rem | 400 | General data, descriptions, and labels. |
| **Label** | `label-sm` | 0.6875rem | 600 | Metadata, caps-styling for category tags. |

**Editorial Note:** Use `on_surface_variant` (#50453E) for body text to reduce harsh contrast against the cream background, creating a softer, more sophisticated reading experience.

---

## 4. Elevation & Depth: Tonal Layering

Traditional shadows and borders are replaced by **Tonal Layering** to create a modern, high-end feel.

- **The Layering Principle:** Depth is achieved by "stacking." A `surface-container-lowest` card placed on a `surface-container-low` background creates a soft, natural lift without the need for heavy shadows.
- **Ambient Shadows:** For floating elements (e.g., active dropdowns), use "Ambient Shadows": `0px 12px 32px rgba(85, 55, 34, 0.06)`. The tint is derived from our `primary` color, not pure black, to mimic natural light filtered through a café window.
- **The "Ghost Border" Fallback:** If a container requires a boundary (e.g., an input field), use the `outline_variant` (#D4C3BA) at **20% opacity**. 100% opaque borders are strictly forbidden.
- **Glassmorphism:** Use `surface_bright` with a 12px blur for navigation bars to allow the "creamy" background colors to bleed through as the user scrolls.

---

## 5. Components: Practical Sophistication

### Buttons
- **Primary:** `primary` background with `on_primary` text. `xl` roundedness (0.75rem). No border.
- **Secondary:** `secondary_container` background. Provides a "latte-like" soft contrast.
- **State:** On hover, shift background to `primary_container`.

### Cards & Lists
- **The "No-Divider" Mandate:** Forbid the use of horizontal rules (`<hr>`). 
- **Separation:** Use 24px/32px of vertical white space or a subtle background shift to `surface-container-high` to separate list items.
- **Roundedness:** Use `xl` (0.75rem) for all main content cards to maintain a friendly yet professional silhouette.

### Input Fields
- **Style:** Background set to `surface-container-lowest` (#FFFFFF).
- **Focus State:** Instead of a thick border, use a 2px "Ghost Border" of `primary` at 40% opacity and a subtle `primary_fixed` outer glow.
- **Vietnamese Support:** Ensure line-height for `body-md` is at least `1.5` to accommodate tone marks without clipping.

### Custom Coffee Components
- **Roast Status Chips:** Use `tertiary_container` for "Dark Roast" and `secondary_fixed` for "Light Roast" indicators.
- **Inventory Heatmaps:** Use a gradient scale from `surface_container` to `primary` to show stock levels.

---

## 6. Do's and Don'ts

### Do
*   **DO** use generous padding (32px+) inside cards to emphasize the "Premium" feel.
*   **DO** use `surface-dim` for inactive states instead of "grey-out" effects to keep the palette warm.
*   **DO** ensure all Vietnamese diacritics are legible by using the `beVietnamPro` scale exclusively.

### Don't
*   **DON'T** use pure black (#000000). It breaks the warm, organic coffee aesthetic.
*   **DON'T** use sharp corners (`none` or `sm`). The brand is "Sophisticated and Clean," which requires the softness of `lg` and `xl` radii.
*   **DON'T** use 1px dividers. If you feel the need for a line, increase the whitespace instead.