---
name: "anthropics-frontend-design"
description: "Master Anthropic Official Frontend Design Skill. Guidelines for building high-end, responsive, accessible web applications with clean component architecture, modern styling, and visual excellence."
version: 1.0.0
---

# Anthropic Official Frontend Design Skill

This skill defines Anthropic's official design and frontend engineering standards for AI coding agents.

---

## 🏛️ 1. Design Aesthetics & Visual Mandate

- **No Simple/Generic UI:** Plain, unstyled, or basic "MVP" layouts are strictly unacceptable.
- **Executive Dark Palette:** Deep background `#030712`, Card background `#0F172A`, Accent Cyan `#00F0FF`, Accent Gold `#F59E0B`.
- **Modern Typography:** Use modern Google Fonts (`Inter`, `Plus Jakarta Sans`, `Outfit`).
- **Visual Depth:** Multi-layered card depth, glassmorphism (`backdrop-filter: blur(16px)`), subtle radial gradients, and glowing borders.

---

## ⚡ 2. Executive User Experience & The 2-Click Rule

- **Regla de los 2 Clics:** Users must be able to search, filter, and access any session video, presentation, or PDF document in 2 clicks or fewer.
- **Instant Search:** Real-time client-side search filtering without full page reloads.
- **1-Click Resumption:** Prominently display a "Continuar Viendo" hero widget allowing executives to resume video playback or document reading from their exact saved timestamp.

---

## ⚙️ 3. Component Architecture & Code Standards

- **React 19 & TypeScript Strict:** All component props must be explicitly typed using interfaces in `frontend/src/types/`.
- **Single Responsibility:** Separate complex views into decoupled components (`Header`, `FilterBar`, `SessionCard`, `ContinueWatching`, `InAppVideoPlayer`, `InAppDocumentViewer`, `AdminAnalyticsView`).
- **Tailwind CSS Abstractions:** Use structured CSS utility classes and design token classes (`glass-header`, `glass-panel`, `glass-card`, `btn-glow`) rather than ad-hoc inline styles.

---

## ♿ 4. Accessibility & Web Vitals

- **WCAG 2.1 AA Compliance:** Minimum 4.5:1 color contrast ratio.
- **Focus Rings:** Visible keyboard focus indicators (`focus-visible:ring-2 focus-visible:ring-cyan-400`).
- **Semantic HTML5:** Use `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`.
