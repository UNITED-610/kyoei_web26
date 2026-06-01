# Design System Inspired by Leica Camera

> Auto-extracted from `https://leica-camera.com/ja-JP?srsltid=AfmBOoqmfxwjZjLjpAc0cr8UXzFsAcXlsOzvsGGJNtVPKObGY5yObCKy` on 2026-05-22

## 1. Visual Theme & Atmosphere

Clean, minimal, and product-focused with deliberate use of whitespace.

The hero section leads with "Leica Leitzphone" followed by "powered by Xiaomi".

**Key Characteristics:**
- Noto Sans as the heading font (custom web font loaded via @font-face)
- Noto Sans as the body font for all running text
- Heading weight 400
- Light/white background (#ffffff) as the primary canvas
- Primary accent `#888888` used for CTAs and brand highlights
- Sharp corners (0-2px) for a precise, technical aesthetic
- Tags: light, sharp, monochrome, bold-typography, sans-serif

## 2. Color Palette & Roles

### Primary
- **Primary Accent** (`#888888`) · `--color-primary`: Brand color, CTA backgrounds, link text, interactive highlights.
- **Secondary Accent** (`#aaaaaa`) · `--color-secondary`: Secondary brand, hover states, complementary highlights.
- **Background** (`#ffffff`) · `--color-bg`: Page background, primary canvas.

### Text
- **Text Primary** (`#222222`) · `--color-text`: Headings and body text.
- **Text Secondary** (`#666666`) · `--color-text-secondary`: Muted text, captions, placeholders.

### Borders & Surfaces
- **Border** (`#e5e5e5`) · `--color-border`: Dividers, outlines, input borders.

## 3. Typography Rules

- **Heading Font:** `Noto Sans` (web font)
- **Body Font:** `Noto Sans` (web font)

### Type Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing |
|---|---|---|---|---|---|
| H1 | Noto Sans | 76px | 400 | 85.12px | normal |
| H2 | Noto Sans | 54px | 400 | 59.4px | normal |
| H3 | Noto Sans | 20px | 600 | 28px | normal |
| H4 | Noto Sans | 14px | 700 | 18.2px | normal |
| Body | Noto Sans | 20px | 400 | 28px | normal |
| Small | Noto Sans | 14px | 400 | 20px | normal |

### Type Scale

| Token | Size | Suggested Usage |
|---|---|---|
| Display | `54px` | headings |
| H1 | `20px` | headings |
| H2 | `18px` | headings |
| H3 | `16px` | headings |

### Japanese Typography (CJK)

This site uses Japanese (CJK) text. Apply the following rules:

- **Line height:** Use `1.7`–`2.0` for body text (CJK needs more vertical space than Latin)
- **Letter spacing:** Use `0.04em`–`0.08em` for body text (improves Japanese readability)
- **Font fallback:** Always include a Japanese font fallback: `Noto Sans, "Noto Sans JP", "Hiragino Kaku Gothic ProN", "Yu Gothic", sans-serif`
- **Word break:** Use `word-break: normal` and `overflow-wrap: anywhere` — never `break-all` for Japanese
- **Kinsoku (禁則処理):** Avoid line breaks before closing brackets 」）】 or after opening brackets 「（【
- **Heading line-height:** `1.3`–`1.5` (tighter than body, but looser than Latin headings)
- **Minimum body font size:** `14px` (Japanese characters are complex, smaller is hard to read)

## 4. Component Stylings

### Card

```css
.card {
  background: #f5f5f5;
  border-radius: 0px;
  padding: 0px;
  box-shadow: rgba(0, 0, 0, 0) 0px 0px 0px 0px, rgba(0, 0, 0, 0) 0px 0px 0px 0px, rgba(34, 34, 34, 0.2) 4px 4px 8px 0px;
}
```

## 5. Layout Principles

- **Base spacing unit:** `20px` — use multiples (40px, 60px, 80px, etc.)

### Spacing Scale (extracted from real elements)

| Token | Value | Role |
|---|---|---|
| spacing-1 | `20px` | element |
| spacing-2 | `24px` | card |
| spacing-3 | `72px` | section |
| spacing-4 | `16px` | element |
| spacing-5 | `12px` | element |
| spacing-6 | `14px` | element |
| spacing-7 | `32px` | card |

### Border Radius Scale

| Token | Value | Element |
|---|---|---|

## 6. Depth & Elevation

No prominent box-shadows detected. This design likely uses flat surfaces with borders or background color changes for depth.

## 7. Do's and Don'ts

### Do
- Use `#ffffff` as the primary background color
- Use `Noto Sans` for all headings and `Noto Sans` for body text
- Use `#888888` as the single dominant accent/CTA color
- Maintain `20px` as the base spacing unit — all gaps should be multiples
- Keep corners sharp (0-2px radius) for a precise, technical feel
- Make headlines large and bold — typography is the hero element
- Stick to grayscale + `#888888` accent — avoid color overload
- Use weight 400 for headings to match the brand's typographic voice
- Use `line-height: 1.7-2.0` for Japanese body text
- Include Japanese font fallback (Noto Sans JP, Hiragino, Yu Gothic)

### Don't
- Don't use colors outside the extracted palette without justification
- Don't substitute Noto Sans/Noto Sans with generic alternatives
- Don't use irregular spacing — stick to 20px grid
- Don't use dark/black backgrounds — this is a light-themed design
- Don't use large border-radius — keep everything crisp and geometric
- Don't add additional saturated colors beyond the primary accent
- Don't use pure black (#000000) for text — use `#222222` instead
- Don't add decorative elements not present in the original design — no badges, ribbons, banners, or ornaments unless the source site uses them
- Don't invent UI patterns the source site doesn't have — if the original has no NEW badge, don't add one just because a red is in the palette
- Don't use `word-break: break-all` for Japanese text — it breaks in the middle of words
- Don't set body font size below 14px for Japanese — characters are too complex
- Don't use Latin-optimized line-height (1.2-1.4) for Japanese body text

## 8. Responsive Behavior

| Breakpoint | Width | Notes |
|---|---|---|
| Mobile | < 640px | Single column, stack sections, reduce font sizes ~80% |
| Tablet | 640–1024px | 2-column where appropriate, maintain spacing ratios |
| Desktop | 1024–1440px | Full layout as designed |
| Wide | > 1440px | Max-width container, center content |

- Touch targets: minimum 44×44px on mobile
- Maintain 20px base unit across breakpoints — only scale multipliers

## 9. Agent Prompt Guide

### Quick Color Reference

```
Background:  #ffffff
Text:        #222222
Accent:      #888888
Secondary:   #aaaaaa
Border:      #e5e5e5
```

### Example Prompts

1. "Build a hero section with a `#ffffff` background, `Noto Sans` heading in `#222222`, and a `#888888` CTA button."
2. "Create a pricing card using background `#ffffff`, border `#e5e5e5`, `Noto Sans` for text, and 60px padding."
3. "Design a navigation bar — `#ffffff` background, `#222222` links, `#888888` for active state."
4. "Build a feature grid with 3 columns, 60px gap, each card using the card component style."
5. "Create a footer with `#222222` background, `#ffffff` text, and 40px padding."

### Iteration Guide

1. Start with layout structure (sections, grid, spacing)
2. Apply colors from the palette — background first, then text, then accents
3. Set typography — font families, sizes from the type scale, weights
4. Add components — buttons, cards, inputs using the specs above
5. Apply border-radius consistently across all elements
6. Check responsive behavior — test mobile and tablet layouts
7. Final pass — verify all colors match, spacing is consistent, fonts are correct

## 10. CSS Custom Properties

> 34 custom properties extracted from `:root` / `html` stylesheets.

### Color Variables

| Variable | Value |
|---|---|
| `--color-dark-red` | `#b5050e` |

### Spacing Variables

| Variable | Value |
|---|---|
| `--container` | `1920px` |
| `--container-max` | `2560px` |
| `--container-narrow-desktop` | `880px` |
| `--container-narrow-tablet` | `600px` |
| `--container-narrow` | `315px` |
| `--header-height` | `88px` |

### Other Variables

| Variable | Value |
|---|---|
| `--color-leica-red` | `226 6 18` |
| `--color-black` | `0 0 0` |
| `--color-white` | `255 255 255` |
| `--color-warm-black` | `34 34 34` |
| `--color-dark-grey` | `142 144 143` |
| `--color-light-grey` | `209 212 211` |
| `--color-grey-050` | `245 245 245` |
| `--color-grey-100` | `231 231 231` |
| `--color-grey-200` | `209 209 209` |
| `--color-grey-300` | `181 180 180` |
| `--color-grey-400` | `154 153 153` |
| `--color-grey-500` | `130 130 130` |
| `--color-grey-600` | `108 108 108` |
| `--color-grey-700` | `51 51 51` |
| `--color-grey-800` | `31 31 31` |
| ... | *(12 more)* |
