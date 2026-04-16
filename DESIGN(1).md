# Design System Specification: The Analytic Editorial

## 1. Overview & Creative North Star
**Creative North Star: The Intelligent Layer**
This design system moves away from the rigid, boxy constraints of traditional academic portals. Instead, it adopts a "High-End Editorial" approach that mirrors the precision of Business Analytics and the prestige of Management Information Systems. We treat the interface not as a flat screen, but as a series of **intelligent layers**. 

By utilizing intentional asymmetry, expansive negative space, and overlapping elements, we create a sense of "Data-In-Motion." The experience should feel like a premium financial journal—authoritative, clean, and technologically sophisticated. We honor the UMD Duluth heritage not through bright primary colors, but through deep, tonal "Old World" maroons contrasted against "New World" tech-teals.

---

## 2. Colors: Tonal Depth vs. Structural Lines
Our palette is rooted in a "Low-Contrast Professionalism" philosophy. We do not use borders to define space; we use light.

### The "No-Line" Rule
**1px solid borders are strictly prohibited for sectioning.** Boundaries must be defined solely through background color shifts or subtle tonal transitions. A section transition should feel like a change in paper stock, not a drawn line.

### Surface Hierarchy & Nesting
Depth is achieved by nesting `surface-container` tiers. 
*   **Base:** `surface` (#f9f9fc) for the primary page background.
*   **The Inset:** Use `surface-container-low` (#f3f3f6) to define secondary content zones.
*   **The Hero:** Use `surface-container-lowest` (#ffffff) for high-focus cards to create a "pop" against the off-white background.

### The "Glass & Gradient" Rule
To bridge the gap between "Business" and "Tech," use Glassmorphism for floating navigation and modal overlays.
*   **Token:** `surface` at 80% opacity with a `20px` backdrop-blur.
*   **Signature Texture:** Use a linear gradient from `primary` (#570000) to `primary_container` (#800000) for hero actions. This prevents the maroon from feeling "flat" and adds a liquid, premium sheen.

---

## 3. Typography: The Corporate Voice
We pair the geometric precision of **Manrope** for displays with the hyper-legibility of **Inter** for data-heavy body text.

*   **Display (Manrope):** Set at `display-lg` (3.5rem) with tight letter-spacing (-0.02em). Use this for hero statements where business meets technology.
*   **Headlines (Manrope):** `headline-md` (1.75rem) should be used for section headers, paired with `tertiary` (#002c2c) to provide a "charcoal-teal" sophistication that feels more modern than pure black.
*   **Body (Inter):** All body copy defaults to `body-lg` (1rem). It provides a neutral, stable foundation for complex information.
*   **Labels (Inter):** `label-md` (0.75rem) in All-Caps with +0.05em tracking for category tags and "Business Analytics" metadata.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "heavy" for a sophisticated analytics brand. We use **Ambient Light** principles.

*   **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` section. This create a "Soft Lift" that is felt rather than seen.
*   **Ambient Shadows:** For floating elements (e.g., active dropdowns), use a multi-layered shadow:
    *   `0px 4px 20px rgba(26, 28, 30, 0.04)`
    *   `0px 10px 40px rgba(26, 28, 30, 0.06)`
*   **The "Ghost Border" Fallback:** If accessibility requires a container edge, use `outline-variant` (#e2bfb9) at **15% opacity**. It should be a whisper of a line, never a shout.

---

## 5. Components

### Cards (Editorial Layout)
*   **Structure:** No dividers. Use 2rem (32px) of internal padding.
*   **Visuals:** Use `surface-container-lowest` for the background.
*   **Interaction:** On hover, the card should not move up; instead, the `outline` should shift from 0% to 20% opacity, and the internal image should scale slightly (1.05x).

### Buttons (The "Call to Intelligence")
*   **Primary:** A gradient of `primary` to `primary_container`. Roundedness: `md` (0.375rem). Text: `on_primary` (White).
*   **Secondary:** `surface_container_high` background with `on_surface` text. No border.
*   **Tertiary (Ghost):** No background. Text in `tertiary` (#002c2c) with an underline that appears only on hover.

### Forms & Inputs
*   **Fields:** Background `surface_container_low`. Bottom-border only (2px) using `outline_variant`.
*   **Focus State:** The bottom border transitions to `tertiary` (Teal), and the background shifts to `surface_container_lowest`.
*   **Error:** Use `error` (#ba1a1a) text for helper messages, never the input box itself, to maintain a clean aesthetic.

### Navigation
*   **The "Analytic Rail":** For desktop, use a slim left-side rail or a floating centered top-nav.
*   **Blur:** Must use the Glassmorphism rule (80% opacity + blur) to allow content to scroll elegantly beneath it.

---

## 6. Do’s and Don’ts

### Do
*   **DO** use `tertiary` (Teal) as a surgical accent for data points, links, and icons.
*   **DO** use generous whitespace. If a section feels crowded, double the padding.
*   **DO** overlap elements (e.g., an image slightly breaking the boundary of a container) to create a custom, "non-template" feel.

### Don’t
*   **DON'T** use 100% black. Use `on_surface` (#1a1c1e) for text to maintain a high-end, ink-on-paper feel.
*   **DON'T** use standard 1px grey dividers. Use vertical space or a `surface` color shift to separate thoughts.
*   **DON'T** use "UMD Yellow" in large blocks. Use `secondary_container` (#fec324) sparingly—only for highlights, "New" tags, or critical alerts.