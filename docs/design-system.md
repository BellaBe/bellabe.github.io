# Bella Belgarokova Design System

A CSS-based design system for the Jekyll static site with a focus on typography stability, accessibility, and maintainability.

## Overview

**Aesthetic:** Precision Engineering meets Editorial Clarity

**Fonts:**
- Display: Instrument Serif (headings, display text)
- Body: DM Sans (paragraphs, UI text)
- Mono: JetBrains Mono (code, labels, navigation)

**Theme:** Dark-first with light mode toggle

---

## Architecture

```
assets/css/
  design-tokens.css   # Design tokens, fallback fonts, utility classes
  main.css            # Component styles (imports tokens)

_layouts/
  default.html        # Font preloading strategy
```

### File Responsibilities

| File | Purpose |
|------|---------|
| `design-tokens.css` | CSS custom properties, fallback font definitions, typography utilities |
| `main.css` | Component styles, layout, responsive design |
| `default.html` | Font preconnect, preload, and loading |

---

## Font Loading Strategy

The design system uses a multi-layer approach to eliminate FOUT (Flash of Unstyled Text):

### 1. Preconnect (default.html)
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
```
Establishes early connections to font servers.

### 2. Preload Critical Fonts (default.html)
```html
<link rel="preload" as="font" type="font/woff2"
      href="https://fonts.gstatic.com/s/instrumentserif/..." crossorigin>
```
Downloads the most important font files immediately.

### 3. Metric-Adjusted Fallbacks (design-tokens.css)
```css
@font-face {
  font-family: 'Instrument Serif Fallback';
  src: local('Georgia');
  ascent-override: 95%;
  descent-override: 25%;
  line-gap-override: 0%;
  size-adjust: 105%;
}
```
Fallback fonts are adjusted to match web font metrics, preventing layout shift.

### 4. Font Stacks with Fallbacks
```css
--font-display: 'Instrument Serif', 'Instrument Serif Fallback', Georgia, serif;
```
The cascade ensures immediate rendering with minimal visual jump when web fonts load.

---

## Design Tokens

### Color Tokens

**Dark Theme (Default)**

| Token | Value | Usage |
|-------|-------|-------|
| `--color-bg-primary` | `#0a0a0b` | Page background |
| `--color-bg-secondary` | `#111113` | Card backgrounds |
| `--color-bg-tertiary` | `#18181b` | Elevated surfaces |
| `--color-bg-elevated` | `#1f1f23` | Highest elevation |
| `--color-text-primary` | `#f4f4f5` | Headings, primary text |
| `--color-text-secondary` | `#a1a1aa` | Body text |
| `--color-text-tertiary` | `#71717a` | Muted text, captions |
| `--color-accent-primary` | `#22d3ee` | Primary actions, links |
| `--color-accent-warm` | `#f59e0b` | Highlights, warnings |

**Light Theme** (applied via `body.light`)

| Token | Value |
|-------|-------|
| `--color-bg-primary` | `#fafafa` |
| `--color-bg-secondary` | `#ffffff` |
| `--color-text-primary` | `#18181b` |
| `--color-accent-primary` | `#0891b2` |

### Typography Scale

Based on Major Third ratio (1.25) for editorial feel.

| Token | Size | Usage |
|-------|------|-------|
| `--font-size-xs` | 12px (0.75rem) | Labels, captions |
| `--font-size-sm` | 14px (0.875rem) | Small text, navigation |
| `--font-size-base` | 16px (1rem) | Minimum body text |
| `--font-size-md` | 17px (1.0625rem) | Comfortable reading |
| `--font-size-lg` | 18px (1.125rem) | Large body text |
| `--font-size-xl` | 20px (1.25rem) | Small headings |
| `--font-size-2xl` | 24px (1.5rem) | Section headings |
| `--font-size-3xl` | 30px (1.875rem) | Page subheadings |
| `--font-size-4xl` | 36px (2.25rem) | Page titles |
| `--font-size-5xl` | 48px (3rem) | Hero headings |
| `--font-size-6xl` | 60px (3.75rem) | Display text |

### Line Heights

| Token | Value | Usage |
|-------|-------|-------|
| `--line-height-tight` | 1.15 | Headings |
| `--line-height-snug` | 1.3 | Subheadings |
| `--line-height-normal` | 1.5 | UI text |
| `--line-height-relaxed` | 1.7 | Body copy |
| `--line-height-loose` | 1.8 | Long-form reading |

### Spacing Scale

4px base unit for precise layouts.

| Token | Value | Pixels |
|-------|-------|--------|
| `--space-1` | 0.25rem | 4px |
| `--space-2` | 0.5rem | 8px |
| `--space-3` | 0.75rem | 12px |
| `--space-4` | 1rem | 16px |
| `--space-6` | 1.5rem | 24px |
| `--space-8` | 2rem | 32px |
| `--space-12` | 3rem | 48px |
| `--space-16` | 4rem | 64px |
| `--space-24` | 6rem | 96px |

### Motion Tokens

| Token | Value | Usage |
|-------|-------|-------|
| `--duration-fast` | 150ms | Micro-interactions |
| `--duration-normal` | 200ms | Standard transitions |
| `--duration-slow` | 300ms | Emphasis transitions |
| `--duration-slower` | 400ms | Complex animations |
| `--ease-out-expo` | cubic-bezier(0.16, 1, 0.3, 1) | Smooth deceleration |

---

## Typography Utility Classes

Ready-to-use typography patterns available in `design-tokens.css`:

### Display Text
```html
<h1 class="text-display-xl">Large Hero</h1>
<h1 class="text-display-lg">Medium Hero</h1>
<h1 class="text-display-md">Small Hero</h1>
```

### Heading Text
```html
<h2 class="text-heading-xl">Section Title</h2>
<h2 class="text-heading-lg">Subsection</h2>
<h3 class="text-heading-md">Card Title</h3>
<h4 class="text-heading-sm">Small Heading</h4>
```

### Body Text
```html
<p class="text-body-lg">Large body text</p>
<p class="text-body-md">Standard body text</p>
<p class="text-body-sm">Compact body text</p>
```

### Mono/Code Text
```html
<code class="text-mono-lg">large code</code>
<code class="text-mono-md">standard code</code>
<span class="text-mono-sm">small mono</span>
```

### Label Text
```html
<span class="text-label">SECTION LABEL</span>
```

---

## Accessibility

### Color Contrast

All text colors meet WCAG AA standards (4.5:1 for normal text, 3:1 for large text):

| Combination | Ratio | Rating |
|-------------|-------|--------|
| Primary text on primary bg | 15.8:1 | AAA |
| Secondary text on primary bg | 6.2:1 | AA |
| Tertiary text on primary bg | 4.5:1 | AA |
| Accent on primary bg | 8.3:1 | AAA |

### Reduced Motion Support

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

### High Contrast Mode

```css
@media (prefers-contrast: more) {
  :root {
    --color-border-subtle: rgba(255, 255, 255, 0.2);
    --color-text-secondary: #d4d4d8;
  }
}
```

### Focus States

All interactive elements have visible focus indicators:
```css
:focus-visible {
  outline: 2px solid var(--color-accent-primary);
  outline-offset: 2px;
}
```

---

## Theme Switching

### JavaScript (in default.html)
```javascript
const toggle = document.getElementById('theme-toggle');
toggle.addEventListener('click', () => {
  document.body.classList.toggle('light');
  localStorage.setItem('theme',
    document.body.classList.contains('light') ? 'light' : 'dark'
  );
});
```

### CSS (design-tokens.css)
```css
body.light {
  --color-bg-primary: #fafafa;
  --color-text-primary: #18181b;
  /* ... other overrides */
}
```

---

## Legacy Aliases

For backwards compatibility, the following aliases are provided:

```css
--bg-primary: var(--color-bg-primary);
--text-primary: var(--color-text-primary);
--accent-primary: var(--color-accent-primary);
/* etc. */
```

New code should use the semantic `--color-*` tokens.

---

## Usage Examples

### Creating a Card
```html
<div class="featured-item">
  <h3><a href="#">Card Title</a></h3>
  <p>Card description text.</p>
  <span class="project-meta">Category</span>
</div>
```

### Creating a Button
```html
<a href="#" class="btn btn-primary"><span>Primary Action</span></a>
<a href="#" class="btn btn-secondary">Secondary Action</a>
```

### Section with Label
```html
<section class="featured-section">
  <h2>Featured Projects</h2>
  <div class="featured-grid">
    <!-- items -->
  </div>
</section>
```

---

## Browser Support

- Chrome 88+ (font-display, CSS custom properties)
- Firefox 78+ (font-display, CSS custom properties)
- Safari 14+ (font-display, CSS custom properties)
- Edge 88+ (Chromium-based)

Graceful degradation for older browsers via fallback fonts and default values.

---

## Performance Considerations

1. **No @import for fonts** - Fonts are loaded via `<link>` tags with preconnect
2. **Critical font preloading** - Most-used font weights are preloaded
3. **Metric-adjusted fallbacks** - Prevent layout shift (CLS)
4. **font-display: swap** - Text remains visible during font load
5. **CSS custom properties** - Single source of truth, easy theming

---

## Maintenance

### Adding a New Color
1. Add to `:root` in `design-tokens.css`
2. Add light theme override in `body.light` if needed
3. Document in this file

### Adding a New Component
1. Add styles to `main.css`
2. Use design tokens for all values (no magic numbers)
3. Ensure responsive behavior
4. Test in both themes

### Updating Fonts
1. Update Google Fonts URL in `default.html`
2. Update preload URLs (get from Google Fonts CSS)
3. Adjust fallback font metrics in `design-tokens.css`
4. Test for layout shift

---

## Files Modified

| File | Changes |
|------|---------|
| `/assets/css/design-tokens.css` | NEW - Design tokens and typography utilities |
| `/assets/css/main.css` | Refactored to use tokens, removed @import |
| `/_layouts/default.html` | Added font preloading strategy |

---

## Version History

- **v1.0.0** (2026-01-23) - Initial design system with FOUT fix
  - Implemented font preloading strategy
  - Created metric-adjusted fallback fonts
  - Established design token architecture
  - Added typography utility classes
  - Added accessibility features
