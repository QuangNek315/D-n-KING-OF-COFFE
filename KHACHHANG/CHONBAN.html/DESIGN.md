# Design System: The Aromatic Editorial

## 1. Overview & Creative North Star
**Creative North Star: "The Modern Alchemist"**
This design system moves away from the "utility-first" look of standard delivery apps and toward a high-end, editorial experience. It treats coffee not as a commodity, but as a craft. The interface mimics the layout of a premium lifestyle magazine: expansive white space (using our Cream `#FFFDFB` background), intentional asymmetry, and a focus on high-fidelity "hero" photography.

By breaking the rigid grid with overlapping elements—such as a coffee cup image bleeding off the edge of a container—we create a sense of tactile depth. The goal is to make the user feel the warmth of the cafe through their screen, using "The Aromatic Editorial" to guide them through a curated sensory journey rather than a mere transaction.

---

### 2. Colors: Tonal Depth & The "No-Line" Rule
We define space through light and shadow, not through strokes.

*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. To separate a product category from the hero section, use a background shift from `surface` (#fbf9f7) to `surface-container-low` (#f5f3f1).
*   **Surface Hierarchy & Nesting:** Treat the UI as layers of fine parchment. 
    *   **Level 0 (Base):** `surface` (#fbf9f7)
    *   **Level 1 (Sections):** `surface-container-low` (#f5f3f1)
    *   **Level 2 (Cards):** `surface-container-lowest` (#ffffff) to provide a "pop" of brightness.
*   **The "Glass & Gradient" Rule:** For floating headers or navigation bars, use Glassmorphism. Apply `surface` at 80% opacity with a `20px` backdrop-blur. 
*   **Signature Textures:** For primary CTAs (Đặt hàng ngay), use a subtle radial gradient: `primary` (#553722) to `primary-container` (#6f4e37). This adds a "roasted" richness that flat hex codes cannot achieve.

| Role | Token | Hex | Usage |
| :--- | :--- | :--- | :--- |
| **Background** | `surface` | #FBF9F7 | The canvas (Cream). |
| **Primary** | `primary` | #553722 | Brand authority, deep roasted coffee tone. |
| **Accent** | `secondary` | #7D562D | The Gold accent for rewards and highlights. |
| **Surface High** | `surface-container-high`| #E9E8E6 | Used for pressed states or subtle depth. |

---

### 3. Typography: Editorial Authority
We use **Be Vietnam Pro** exclusively. The hierarchy is designed to feel like a premium menu.

*   **Display (Display-LG/MD):** Use for promotional headlines (e.g., "Hương Vị Hoàng Gia"). Set with tight letter-spacing (-0.02em) to feel authoritative.
*   **Headlines (Headline-SM):** Use for category titles (e.g., "Cà Phê Pha Máy").
*   **Body (Body-LG):** The workhorse for product descriptions. High line-height (1.6) is required to maintain the "Editorial" feel.
*   **Labels (Label-MD):** Uppercase with +0.05em tracking, used for metadata like "CÒN HÀNG" or "HOT".

---

### 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are replaced by **Ambient Shadows** and **Tonal Lift**.

*   **The Layering Principle:** To highlight a "Special Offer" card, do not add a border. Place a `surface-container-lowest` (#ffffff) card on top of a `surface-container-low` (#f5f3f1) background. The subtle contrast is enough for the eye.
*   **Ambient Shadows:** For floating action buttons (FAB), use a shadow color derived from the brand: `rgba(85, 55, 34, 0.08)` with a `30px` blur. It should look like a soft glow, not a dark stain.
*   **The "Ghost Border":** If a button sits on a similarly colored image, use `outline-variant` (#d4c3ba) at **15% opacity**. It provides just enough "edge" without breaking the editorial flow.

---

### 5. Components

#### **Buttons**
*   **Primary (Chính):** Rounded-xl (1.5rem), `primary` background, `on-primary` (#ffffff) text. Use for the final "Thanh toán" action.
*   **Secondary (Phụ):** Rounded-xl, `secondary_container` (#ffca98) background. Used for "Thêm vào giỏ hàng".
*   **Tertiary:** No background; `primary` text with a subtle underline in `secondary`.

#### **Cards (Sản phẩm)**
*   **Structure:** No dividers. Use a `1.5rem` (xl) corner radius.
*   **Layout:** Use a 2-column asymmetric grid. One card might be taller than the other to showcase the "Drink of the Month," breaking the repetitive "gallery" feel.

#### **Input Fields (Tìm kiếm)**
*   **Style:** Minimalist. Use `surface-container-high` as a solid background fill with no border. 
*   **State:** On focus, the background shifts to `surface-container-lowest` with a `secondary` (Gold) ghost border.

#### **App-Specific Components**
*   **Scent-Visualizer (Visual Đặc trưng):** A small, animated "steam" element using semi-transparent `secondary` gradients that appears behind high-quality coffee images.
*   **The Royal Bar (Thanh Trạng Thái):** A persistent bottom sheet for "Giỏ hàng" using Glassmorphism, allowing the cream background to peek through.

---

### 6. Do's and Don'ts

#### **Do:**
*   **DO** use Vietnamese characters with proper diacritics—ensure line-height accounts for the "Be Vietnam Pro" stacked accents.
*   **DO** use high-quality, "food-porn" style photography. The image should be the hero; the UI is the frame.
*   **DO** utilize the full width of the screen. Let images bleed to the edges to create a "boundless" feeling.

#### **Don't:**
*   **DON'T** use pure black (#000000). Always use `on-surface` (#1b1c1b) or `primary` (#553722) for text.
*   **DON'T** use 1px dividers. If you feel the need for a line, use `24px` of white space instead.
*   **DON'T** use sharp corners. Use the `Roundedness Scale` (Default: 0.5rem, Cards/Buttons: 1.5rem) to maintain a soft, organic, and appetizing feel.

---
**Language Note:** All customer-facing strings must be in Vietnamese.
*   *Example:* "Add to Cart" -> "Thêm vào giỏ"
*   *Example:* "Order History" -> "Lịch sử đơn hàng"
*   *Example:* "Royal Member" -> "Thành viên Hoàng gia"