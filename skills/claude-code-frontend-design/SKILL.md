---
name: "claude-code-frontend-design"
description: "Master Claude Code Frontend Design Plugin Rules. Detailed specifications for layout systems, Tailwind CSS integration, state management, HTTP Range video streaming, and DLP Signed URL document security."
version: 1.0.0
---

# Claude Code Frontend Design Plugin Rules

This skill incorporates the rules and component patterns from Claude Code's official `plugins/frontend-design` module.

---

## 🎨 1. Design Token Integration & CSS Variables

- **Variables:** Define CSS tokens in `:root` (`--bg-primary`, `--bg-surface`, `--bg-card`, `--breca-cyan`, `--breca-blue`, `--breca-gold`).
- **Utility Classes:** Wrap complex glassmorphism, blur, and border styles into reusable utility classes.
- **Dark Mode Optimization:** Ensure dark background surfaces feature subtle ambient radial gradients to eliminate flat black appearance.

---

## 🚀 2. State & Media Component Patterns

- **Custom Video Player (`InAppVideoPlayer.tsx`):**
  - Custom progress seekbar with cyan gradient fill.
  - Playback speed selector (`1x`, `1.25x`, `1.5x`, `2x`).
  - Auto-saving timestamp progress (`onUpdateProgress`).
  - HTTP Range 206 progressive video streaming.

- **Custom Document Viewer (`InAppDocumentViewer.tsx`):**
  - Page navigation and page count indicators.
  - Dynamic zoom controls (`50%` to `200%`).
  - Full-screen viewing toggle.
  - DLP Signed URL download button with 15-minute short TTL expiration.

---

## 📊 3. Executive Analytics & Dashboard Patterns

- **KPI Metrics:** Summary cards for active leaders, total hours watched, retention rate, and subsidiary participation.
- **Progress Distribution Bars:** Visual breakdown by Breca subsidiary (*Minsur, Rímac, Centria, BBVA Breca, Urbanova, TASA, Clínica Internacional, Copsa*).
