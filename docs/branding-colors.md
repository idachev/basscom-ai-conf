# BASSCOM AI Conference 2026 — Branding Colors

Source: `https://www.basscom-ai-conf.com` (extracted from live CSS custom properties and computed styles).

## Primary Palette

| Role | Hex | CSS Variable | Usage |
|---|---|---|---|
| Teal (brand primary) | `#1a7a7a` | `--teal` | Main accent — links, highlights, section markers |
| Teal Light | `#0d8a8a` | `--teal-light` | Hover / variant |
| Teal Dark | `#14605f` | `--teal-dark` | Deeper accents |
| Teal Tint | `rgba(26, 122, 122, 0.08)` | `--teal-bg` | Subtle section backgrounds |

## Neutrals

| Role | Hex | CSS Variable | Usage |
|---|---|---|---|
| Text (primary) | `#2d3436` | `--text` | Body copy, headings |
| Text Light | `#636e72` | `--text-light` | Secondary text |
| Text Lighter | `#b2bec3` | `--text-lighter` | Muted / disabled |
| Background | `#f5f7fa` | `--bg` | Page background |
| Surface (white) | `#ffffff` | `--bg-white` | Cards, nav |
| Border | `#dfe6e9` | `--border` | Dividers, card borders |

## Secondary / Accent

| Role | Hex | Usage |
|---|---|---|
| Terracotta / Copper | `#cc785c` | Secondary accent (buttons, highlights) |
| Terracotta Dark | `#b05f44` | Hover for copper accent |
| Bronze | `#cd7f32` | Sponsor-tier badge |
| Gold | `#d4a017` / `#b8860b` | Sponsor-tier badge |
| Brown | `#8b5e3c` | Tertiary accent |

## Signature Gradients

**Hero overlay** — fades white to teal tint:

```css
linear-gradient(
  rgba(255, 255, 255, 0.92) 0%,
  rgba(245, 247, 250, 0.88) 40%,
  rgba(224, 240, 240, 0.82) 70%,
  rgba(26, 122, 122, 0.15) 100%
);
```

**Divider glow** — horizontal copper accent:

```css
linear-gradient(
  transparent 0%,
  rgba(204, 120, 92, 0.45) 50%,
  transparent 100%
);
```

## Design Tokens (as defined on `:root`)

```css
:root {
  --teal: #1a7a7a;
  --teal-light: #0d8a8a;
  --teal-dark: #14605f;
  --teal-bg: rgba(26, 122, 122, 0.08);

  --text: #2d3436;
  --text-light: #636e72;
  --text-lighter: #b2bec3;

  --bg: #f5f7fa;
  --bg-white: #ffffff;
  --border: #dfe6e9;

  --radius: 12px;
  --radius-sm: 8px;
  --nav-height: 72px;

  --shadow: 0 2px 16px rgba(0, 0, 0, 0.06);
  --shadow-lg: 0 8px 32px rgba(0, 0, 0, 0.1);
}
```

## Summary

Teal primary (`#1a7a7a`) paired with a warm copper accent (`#cc785c`) on a near-white (`#f5f7fa`) background with dark-slate text (`#2d3436`). Sponsor tiers introduce bronze/gold/brown tones.
