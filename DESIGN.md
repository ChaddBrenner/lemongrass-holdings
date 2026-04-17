# Design System Documentation: Organic Editorial

## 1. Overview & Creative North Star
The objective of this design system is to move Lemongrass Investments away from the cold, spreadsheet-driven aesthetic of traditional real estate and into the realm of **"Organic Editorial."** 

This system is built on the philosophy of the **Digital Curator**. We are not just showing properties; we are presenting a lifestyle of growth and stability. We achieve this through "intentional asymmetry"—breaking the rigid 12-column grid with overlapping elements and generous white space—and a high-contrast typographic scale that mirrors premium architectural journals. The goal is a UI that feels "grown," not "built," utilizing soft tonal shifts rather than harsh structural lines.

---

## 2. Color Strategy: Tonal Sophistication
This palette transitions from the deep, grounded greens of botanical life to the airy, warm neutrals of a sunlit studio.

### The "No-Line" Rule
To maintain a high-end feel, **1px solid borders are strictly prohibited for sectioning content.** We define boundaries through:
- **Background Shifts:** Moving from `surface` to `surface-container-low`.
- **Typographic Anchors:** Using bold `display-sm` headings to "hold" a section’s space.
- **Negative Space:** Increasing padding to create a psychological "stop" for the eye.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of heavy-stock paper.
- **Base Layer:** `background` (#fafaf5).
- **Secondary Sections:** `surface-container-low` (#f4f4ef).
- **Interactive/Floating Cards:** `surface-container-lowest` (#ffffff) to provide a "lifted" appearance.
- **Nested Detail Containers:** Use `surface-container-high` (#e8e8e3) inside a `surface-container` to draw focus to technical data or secondary forms.

### Glass & Gradient (Signature Polish)
For floating navigation bars or premium property overlays, use **Glassmorphism**: 
- Background: `surface` at 70% opacity.
- Backdrop-blur: `12px` to `20px`.
- This ensures the brand’s natural greens bleed through the interface, making the UI feel integrated with the content.

For Primary CTAs, use a subtle **Signature Gradient** from `primary` (#526528) to `primary_container` (#8da25e) at a 135-degree angle to add "soul" and depth to the interaction point.

---

## 3. Typography: The Editorial Voice
Our type pairing creates a tension between tradition and modernity.

- **The Headliner (Newsreader):** This serif is our "Trust" factor. It should be used for all `display` and `headline` levels. It mimics the masthead of a prestigious investment report.
- **The Engine (Manrope):** This sans-serif is our "Clarity" factor. Used for `title`, `body`, and `label` roles. Its high legibility ensures that complex investment data remains approachable.

**Visual Hierarchy Tip:** Use `display-lg` sparingly for hero statements. The contrast between a massive `display-lg` headline and a restrained `body-md` description is what creates the "Editorial" high-fashion look.

---

## 4. Elevation & Depth: Tonal Layering
We eschew the standard "drop shadow" in favor of natural light physics.

### The Layering Principle
Depth is achieved by stacking. Place a `surface-container-lowest` card on top of a `surface-container-low` background. This creates a soft, natural lift that feels architectural rather than digital.

### Ambient Shadows
When a card must float (e.g., a modal or a primary property card), use an **Ambient Shadow**:
- **Color:** Use `on_surface` (#1a1c19) at 6% opacity.
- **Blur:** 24px - 40px.
- **Offset:** Y: 8px.
- This mimics natural, diffused sunlight rather than a computer-generated shadow.

### The "Ghost Border" Fallback
If a border is required for accessibility (e.g., in high-density data tables), use a **Ghost Border**:
- Token: `outline_variant` (#c6c8b6).
- **Opacity:** Reduced to 20%.
- A 100% opaque border is considered a failure of the design system’s "Organic" philosophy.

---

## 5. Components

### Buttons
- **Primary:** Gradient fill (`primary` to `primary_container`), `on_primary` text. Use `xl` (1.5rem) roundedness for a modern, approachable feel.
- **Secondary:** `surface_container_high` background with `on_surface` text. No border.
- **Tertiary:** Text-only using `label-md` in `primary` color, with a subtle underline on hover.

### Cards
- **Construction:** No dividers. Use 24px - 32px padding to separate header from body.
- **Elevation:** Use Tonal Layering (Surface-container-lowest) with an Ambient Shadow on hover.

### Input Fields
- **Style:** Understated. Use `surface_container` background with a `none` border, but apply a 2px bottom-stroke of `outline` when focused.
- **Labels:** Always use `label-md` in `on_surface_variant` to keep the UI quiet.

### Chips (Selection/Filters)
- Use `secondary_container` for unselected states.
- Use `primary` with `on_primary` text for selected states.
- High roundedness (`full`) is required to contrast against the more structured card layouts.

---

## 6. Do's and Don'ts

### Do
- **Use Intentional Asymmetry:** Offset images from text blocks to create a "scrapbook" editorial feel.
- **Embrace White Space:** If a section feels crowded, double the padding. This is a premium investment brand; it needs room to breathe.
- **Layer Text Over Glass:** Use the glassmorphism rule for captions over property images to maintain legibility without blocking the photography.

### Don't
- **Don't use 1px solid lines:** Never use a line to separate "Header" from "Body." Use a background color shift or whitespace.
- **Don't use pure black:** Use `on_surface` (#1a1c19) for text. Pure black (#000000) is too harsh for the "Organic" theme.
- **Don't over-round everything:** Stick to the `DEFAULT` (0.5rem) for most cards to maintain a professional, architectural structure. Reserve `full` roundedness for interactive elements like buttons and chips.
- **Don't use high-contrast shadows:** If a shadow is clearly visible at a glance, it is too heavy. It should be felt, not seen.