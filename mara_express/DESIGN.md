```markdown
# Design System Document: Super Hamburguesas Mara

## 1. Overview & Creative North Star: "The Culinary Kinetic"
The food delivery space is often a sea of generic white cards and predictable grids. This design system rejects the "template" look in favor of **The Culinary Kinetic**. Our North Star is a high-energy, editorial-inspired experience that feels as fresh and handcrafted as the food itself.

We move beyond standard UI by using **intentional asymmetry**, **overlapping imagery**, and **tonal layering**. The interface isn't just a utility; it’s a digital tabletop. By utilizing "Plus Jakarta Sans" for its aggressive, modern geometric curves and "Be Vietnam Pro" for high-legibility storytelling, we create a signature rhythm that feels premium yet accessible.

---

## 2. Colors & Surface Philosophy

### Color Palette
- **Primary (`#b7102a`):** Our "Sizzling Red." Used for high-action CTAs and brand identifiers.
- **Secondary (`#7d5800`):** Our "Golden Crust." Provides a sophisticated contrast to the red, used for highlights and premium badges.
- **Tertiary (`#00685d`):** Our "Fresh Crisp." Reserved for health-conscious options, "Ready" statuses, and ecological messaging.
- **Surface & Background (`#fff8f7`):** A warm-tinted neutral that avoids the sterile "hospital white" of competitors.

### The "No-Line" Rule
**Borders are prohibited.** We define boundaries through background color shifts. Instead of a 1px line, use the transition between `surface` and `surface-container-low`. This creates a softer, more organic interface that feels cohesive rather than fragmented.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers.
- **Layer 0 (Base):** `surface` or `surface-bright`.
- **Layer 1 (Sections):** `surface-container-low` (for secondary content areas).
- **Layer 2 (Interactive Elements):** `surface-container-lowest` (pure white) for the highest visual "lift" on cards.
- **Layer 3 (Floating):** Semi-transparent `surface-variant` with a 16px `backdrop-blur` for navigation bars and floating action menus.

### Signature Textures
Avoid flat primary colors on large surfaces. Use a subtle linear gradient from `primary` to `primary-container` (at a 135° angle) to give hero sections and main buttons a "soul" and a sense of volume.

---

## 3. Typography: Editorial Impact
We use a high-contrast scale to guide the eye and inject personality into the ordering flow.

*   **Display & Headline (Plus Jakarta Sans):** These are our "shouting" levels. They should be tight-tracked (-0.02em) and bold. Use `display-lg` for hero promotions to make the food feel larger than life.
*   **Title & Body (Be Vietnam Pro):** A humanist sans-serif that balances the aggression of Jakarta. It provides warmth and clarity for menu descriptions and checkout details.
*   **Label (Plus Jakarta Sans):** Small, uppercase, and slightly letter-spaced (+0.05em) for category tags and metadata.

---

## 4. Elevation & Depth: Tonal Layering

### The Layering Principle
Depth is achieved by stacking. A `surface-container-lowest` card sitting on a `surface-container` background creates a natural "lift." Avoid drop shadows unless the element is physically moving over other content.

### Ambient Shadows
When a shadow is required (e.g., a floating "View Cart" button), use an **Extra-Diffused Shadow**:
- **Blur:** 40px to 60px.
- **Color:** `on-surface` at 4% to 6% opacity. 
- **Offset:** Y: 8px.
*Note: Never use pure black (#000) for shadows; use a tinted version of our surface color.*

### Glassmorphism
For floating category headers, use a "Frosted Glass" effect:
- **Background:** `surface-container` at 70% opacity.
- **Effect:** Background blur (20px).
- **Edge:** A "Ghost Border" using `outline-variant` at 15% opacity to catch the light.

---

## 5. Components

### Buttons
- **Primary:** Gradient from `primary` to `primary-container`. Corner radius: `xl` (3rem) for a friendly, pill-like feel. Large touch targets (minimum 56px height).
- **Secondary:** `secondary-fixed-dim` background with `on-secondary-fixed` text.
- **Tertiary:** No background. Text-only with an underline shift on hover.

### Cards (The "Mara" Menu Card)
- **Structure:** No dividers. Use `surface-container-highest` for the image container and `surface-container-lowest` for the content area.
- **Asymmetry:** Let high-quality food imagery "break" the container. A burger should slightly overlap the card's edge to create a 3D effect.
- **Spacing:** Use 24px (1.5rem) internal padding to provide "Breathing Room."

### Chips (Category Selection)
- **Inactive:** `surface-container-high` background, no border.
- **Active:** `secondary-container` background with a subtle pulse animation.
- **Icons:** Use stylized, thick-stroke icons for "Burgers," "Pizzas," and "Fries."

### Input Fields
- **Style:** Understated. Use `surface-container-low` as the fill. 
- **Interaction:** On focus, the background shifts to `surface-container-lowest` and a "Ghost Border" of `primary` (20% opacity) appears.

---

## 6. Do's and Don'ts

### Do:
- **Use "Intentional White Space":** Allow at least 32px of space between major sections to let the high-quality imagery breathe.
- **Embrace Overlaps:** Let a "MARA" logo or a floating fries icon bleed into the next section.
- **Prioritize Accessibility:** Ensure that `on-primary` text always sits on a `primary` background with at least a 4.5:1 contrast ratio.

### Don't:
- **Don't use 1px dividers:** If content needs separating, use a 8px vertical gap or a background color shift.
- **Don't use sharp corners:** Our brand is "friendly." Stick strictly to the `md` to `xl` roundedness scale.
- **Don't clutter the view:** Limit the use of `secondary` (Yellow) and `tertiary` (Green) to functional highlights; don't use them as primary backgrounds.

---

*This design system is a living framework. It is intended to evolve with the brand, but the core principle of **Tonal Depth over Structural Lines** must remain the constant foundation.*```