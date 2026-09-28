---
name: "pbakaus-impeccable"
description: "Master Impeccable Design System & Audit Skill (23 Commands). Provides comprehensive design polish, spatial hierarchy calculations, micro-interaction motion curves, typography scaling, color contrast audits, glassmorphism layering, and component refinement workflows."
version: 1.0.0
---

# Impeccable Design System & Audit Skill (23 Commands)

This skill provides an exhaustive, production-grade design system and auditing instruction set derived from `pbakaus/impeccable`.

---

## 📐 1. Spatial Grid & Layout Systems (`/spatial-grid`, `/fluid-layout`)

- **8pt Base Grid:** All dimensions, margins, paddings, gaps, and heights must be strictly derived from 8px increments (`8px`, `16px`, `24px`, `32px`, `40px`, `48px`, `64px`, `80px`).
- **Responsive Breakpoint Tokens:**
  - `xs`: 0px to 479px (Mobile Vertical)
  - `sm`: 480px to 639px (Mobile Horizontal)
  - `md`: 640px to 767px (Tablets)
  - `lg`: 768px to 1023px (Laptops)
  - `xl`: 1024px to 1279px (Desktops)
  - `2xl`: 1280px+ (Executive Display Monitors)

---

## 🎨 2. Glassmorphism & Depth System (`/glass-depth`, `/dark-mode-glow`)

- **Background Surfaces:** Deep Executive Dark (`#030712`), Translucent Navy Panels (`rgba(15, 23, 42, 0.75)`), Glass Cards (`linear-gradient(135deg, rgba(30, 41, 59, 0.7), rgba(15, 23, 42, 0.6))`).
- **Backdrop Filters:** `backdrop-filter: blur(16px) saturate(1.8)`.
- **Border Accents:** `1px solid rgba(255, 255, 255, 0.08)`. Hover states highlight to Electric Cyan `rgba(0, 240, 255, 0.4)`.
- **Shadow Layers:** Multi-layered diffuse drop shadows `box-shadow: 0 20px 50px -10px rgba(0, 240, 255, 0.15)`.

---

## 🔤 3. Typography & Contrast Audit (`/type-scale`, `/polish-contrast`)

- **Font Family Stack:** `'Inter'`, `'Plus Jakarta Sans'`, system-ui, sans-serif.
- **Fluid Modular Scale (1.25 Ratio):**
  - Body Small: `12px` / `0.75rem`
  - Body Base: `14px` / `0.875rem`
  - Heading 3: `18px` / `1.125rem`
  - Heading 2: `24px` / `1.5rem`
  - Heading 1: `32px` / `2rem`
- **WCAG 2.1 AA Compliance:** Minimum 4.5:1 contrast for normal body text, 3:1 for large display titles against `#030712`.

---

## ⚡ 4. Micro-Interactions & Motion Curves (`/motion-curves`, `/micro-interactions`)

- **Easing Function:** `cubic-bezier(0.16, 1, 0.3, 1)` (Spring-like smooth deceleration).
- **Duration:** 300ms for state transitions.
- **Hover Parallax:** `transform: translateY(-5px) scale(1.01)` on cards.
- **Click Feedback:** Active state `scale(0.98)` compression effect.

---

## 🛠️ 5. The 23 Impeccable Design Commands

1. `/audit-ui` - Full visual hierarchy, contrast, and alignment inspection.
2. `/polish-contrast` - Adjust text/surface hex codes for WCAG AA compliance.
3. `/spatial-grid` - Enforce 8pt padding and margin rules.
4. `/type-scale` - Calculate fluid font sizes and line heights.
5. `/glass-depth` - Ingest multi-layered glassmorphic background & borders.
6. `/motion-curves` - Apply spring animations and bezier curves.
7. `/color-tokens` - Define primary, secondary, and semantic color tokens.
8. `/component-atoms` - Structure Buttons, Inputs, Badges, and Switches.
9. `/component-cards` - Build 3D floating cards with hover elevation.
10. `/micro-interactions` - Add scale, glow, and compression feedback.
11. `/fluid-layout` - Manage container grid across all 6 breakpoints.
12. `/accessibility-focus` - Ensure visible keyboard focus rings.
13. `/touch-targets` - Guarantee >= 44x44px interactive touch targets.
14. `/dark-mode-glow` - Position radial light orbs behind key widgets.
15. `/executive-badges` - Render status pill badges with indicator dots.
16. `/empty-states` - Render informative empty state illustrations.
17. `/loading-skeletons` - Render shimmer animation placeholders.
18. `/form-validation-ui` - Render inline Zod form validation messages.
19. `/modal-overlay` - Construct blurred backdrop dialog overlays.
20. `/header-nav` - Construct translucent navigation bars.
21. `/media-players` - Build custom video and document viewer controls.
22. `/data-kpis` - Build executive metric dashboard panels.
23. `/handoff-tokens` - Export design tokens to CSS and TypeScript.
