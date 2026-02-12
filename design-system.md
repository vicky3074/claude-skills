# Design System Reference

A comprehensive guide for typography, spacing, and color usage based on official design standards from Google Fonts, U.S. Web Design System (USWDS), and industry best practices for 2025.

## System Instructions

When the user asks for design system recommendations, typography guidance, spacing scales, or color palettes, provide specific recommendations from this reference guide. Always specify exact values (hex codes for colors, pixel values for spacing, specific font names).

## Typography Systems

### Professional Font Pairings (Google Fonts)

#### Enterprise/Corporate Websites
1. **Lato + Roboto**
   - Heading: Lato (Bold 600)
   - Body: Roboto (Regular 400)
   - Use case: Professional, clean, highly readable for business sites
   - Example: Headings at 32-48px, Body at 16-18px

2. **Inter + Source Sans Pro**
   - Heading: Inter (Semi-Bold 600)
   - Body: Source Sans Pro (Regular 400)
   - Use case: Modern tech companies, SaaS products
   - Example: Headings at 28-40px, Body at 16-18px

3. **Playfair Display + Montserrat**
   - Heading: Playfair Display (Bold 700) - Serif
   - Body: Montserrat (Regular 400) - Sans-serif
   - Use case: Premium brands, editorial content, luxury products
   - Example: Headings at 36-56px, Body at 16-18px

4. **Poppins + Open Sans**
   - Heading: Poppins (Semi-Bold 600)
   - Body: Open Sans (Regular 400)
   - Use case: Friendly, modern, approachable brands
   - Example: Headings at 30-44px, Body at 16-18px

5. **Raleway + Merriweather**
   - Heading: Raleway (Bold 700) - Sans-serif
   - Body: Merriweather (Regular 400) - Serif
   - Use case: Elegant, traditional businesses, law firms
   - Example: Headings at 32-48px, Body at 17-19px

### Typography Scale (2025 Standards)

**Mobile (320px - 767px)**
- Display: 32-40px (2rem - 2.5rem)
- H1: 28-32px (1.75rem - 2rem)
- H2: 24-28px (1.5rem - 1.75rem)
- H3: 20-24px (1.25rem - 1.5rem)
- Body: 16px (1rem) - NEVER go below this for accessibility
- Small: 14px (0.875rem)

**Tablet (768px - 1023px)**
- Display: 40-56px (2.5rem - 3.5rem)
- H1: 32-40px (2rem - 2.5rem)
- H2: 28-32px (1.75rem - 2rem)
- H3: 24-28px (1.5rem - 1.75rem)
- Body: 17-18px (1.0625rem - 1.125rem)
- Small: 15px (0.9375rem)

**Desktop (1024px+)**
- Display: 56-72px (3.5rem - 4.5rem)
- H1: 40-56px (2.5rem - 3.5rem)
- H2: 32-40px (2rem - 2.5rem)
- H3: 24-32px (1.5rem - 2rem)
- Body: 18-20px (1.125rem - 1.25rem)
- Small: 16px (1rem)

### Typography Rules (USWDS Standards)

**Line Height**
- Display/Headings: 1.1 - 1.3
- Body text: 1.5 - 1.75 (optimal: 1.6)
- Small text: 1.4 - 1.5

**Line Length (Measure)**
- Optimal: 66 characters per line
- Acceptable range: 45-80 characters per line
- Mobile: 35-50 characters per line

**Font Weights**
- Use 2-3 weights maximum (e.g., Regular 400, Semi-Bold 600, Bold 700)
- Avoid using more than 3 weights for performance

**Letter Spacing**
- Headings: -0.02em to -0.01em (tighter)
- Body: 0 (default)
- ALL CAPS: +0.05em to +0.1em (wider)

---

## Spacing Scale (8pt Grid System)

Use multiples of 4px or 8px for all spacing. This creates visual rhythm and consistency.

### Standard Spacing Scale

```
4px   (0.25rem)  - xs   - Minimal spacing, icon gaps
8px   (0.5rem)   - sm   - Tight spacing, button padding
12px  (0.75rem)  - md   - Component spacing
16px  (1rem)     - lg   - Default spacing, paragraph margins
24px  (1.5rem)   - xl   - Section spacing
32px  (2rem)     - 2xl  - Large section spacing
48px  (3rem)     - 3xl  - Major section dividers
64px  (4rem)     - 4xl  - Page section spacing
96px  (6rem)     - 5xl  - Hero sections
128px (8rem)     - 6xl  - Extra large spacing
```

### Spacing Usage Guidelines

**Component Internal Spacing (Padding)**
- Button: 12px vertical, 24px horizontal (py-3 px-6)
- Card: 24px all sides (p-6)
- Input field: 12px vertical, 16px horizontal (py-3 px-4)
- Modal: 32px all sides (p-8)

**Component External Spacing (Margins)**
- Between paragraphs: 16px (mb-4)
- Between sections: 64px (mb-16)
- Between list items: 8px (space-y-2)
- Between cards in grid: 24px (gap-6)

**Container Max Width**
- Content: 1280px (max-w-7xl)
- Text content: 768px (max-w-3xl) - for readability
- Form: 576px (max-w-lg)

---

## Color Systems

### Color Palette Structure

Every design needs:
1. **Primary Color** - Main brand color, CTAs, links
2. **Secondary Color** - Supporting brand color, accents
3. **Neutral Colors** - Backgrounds, text, borders (5-7 shades)
4. **Semantic Colors** - Success, warning, error, info

### Enterprise Color Palettes

#### Professional Blue System
```
Primary:
  - Blue-600: #2563EB (Main brand, CTAs)
  - Blue-700: #1D4ED8 (Hover states)

Secondary:
  - Orange-500: #F97316 (Accents, highlights)
  - Orange-600: #EA580C (Hover)

Neutrals:
  - Slate-950: #020617 (Darkest backgrounds)
  - Slate-900: #0F172A (Dark sections)
  - Slate-800: #1E293B (Cards)
  - Slate-700: #334155 (Borders)
  - Slate-600: #475569 (Disabled text)
  - Slate-400: #94A3B8 (Secondary text)
  - Slate-200: #E2E8F0 (Light borders)
  - Slate-100: #F1F5F9 (Light backgrounds)
  - White: #FFFFFF (Pure white)

Semantic:
  - Success: #10B981 (Green-500)
  - Warning: #F59E0B (Amber-500)
  - Error: #EF4444 (Red-500)
  - Info: #3B82F6 (Blue-500)
```

#### Tech/SaaS Color System
```
Primary:
  - Indigo-600: #4F46E5
  - Indigo-700: #4338CA

Secondary:
  - Purple-500: #A855F7
  - Purple-600: #9333EA

Neutrals: (Same slate scale as above)

Semantic:
  - Success: #22C55E (Green-500)
  - Warning: #EAB308 (Yellow-500)
  - Error: #DC2626 (Red-600)
  - Info: #06B6D4 (Cyan-500)
```

### Color Usage Rules

**Text Colors (WCAG AA Compliant)**
- Primary text on white: Slate-900 (#0F172A) - 14.6:1 ratio
- Secondary text on white: Slate-600 (#475569) - 7.3:1 ratio
- Text on dark: White (#FFFFFF) or Slate-100 (#F1F5F9)
- Minimum contrast ratio: 4.5:1 for body text, 3:1 for large text (24px+)

**Background Colors**
- Light theme main: White (#FFFFFF)
- Light theme alternate: Slate-100 (#F1F5F9)
- Dark theme main: Slate-950 (#020617)
- Dark theme alternate: Slate-900 (#0F172A)

**Interactive Elements**
- Primary CTA: Primary-600 (background), White (text)
- Secondary CTA: White (background), Primary-600 (text), Primary-600 (border)
- Links: Primary-600 (default), Primary-700 (hover)
- Focus states: Add 2px ring with Primary-500 at 50% opacity

**Borders**
- Light theme: Slate-200 (#E2E8F0)
- Dark theme: Slate-700 (#334155)
- Active borders: Primary-600

---

## Responsive Design Breakpoints

Use these standard breakpoints for consistency:

```
Mobile:    320px - 639px   (default, mobile-first)
Tablet:    640px - 1023px  (sm:)
Desktop:   1024px - 1279px (md:)
Large:     1280px+         (lg:)
```

### Tailwind CSS Breakpoints
```
sm: 640px   - tablet
md: 768px   - small desktop
lg: 1024px  - desktop
xl: 1280px  - large desktop
2xl: 1536px - extra large
```

---

## Quick Reference Examples

### Complete Component Styling

**Primary Button**
```css
/* Tailwind Classes */
bg-blue-600 hover:bg-blue-700
text-white font-semibold
px-6 py-3 rounded-lg
transition-all duration-200
shadow-lg hover:shadow-xl
focus:ring-2 focus:ring-blue-500 focus:ring-offset-2
```

**Card Component**
```css
/* Tailwind Classes */
bg-white rounded-xl
p-6 md:p-8
shadow-lg
border border-slate-200
hover:shadow-2xl transition-shadow duration-300
```

**Section Spacing**
```css
/* Tailwind Classes */
py-16 md:py-24 lg:py-32  /* Vertical padding */
px-6 lg:px-8              /* Horizontal padding */
max-w-7xl mx-auto         /* Centered container */
```

---

## Performance Tips

1. **Font Loading**: Use 2-3 font weights maximum
2. **Variable Fonts**: Single file with multiple weights (2025 best practice)
3. **Fluid Typography**: Use clamp() instead of fixed breakpoints
   ```css
   font-size: clamp(1rem, 0.5rem + 2vw, 2rem);
   ```
4. **Color Optimization**: Define CSS custom properties for colors
   ```css
   :root {
     --color-primary: #2563EB;
     --color-secondary: #F97316;
   }
   ```

---

## Accessibility Checklist

- [ ] Minimum 16px body text size
- [ ] 4.5:1 contrast ratio for body text
- [ ] 3:1 contrast ratio for large text (24px+)
- [ ] Line height 1.5+ for body text
- [ ] Line length 45-80 characters
- [ ] Touch targets minimum 44x44px (py-3 px-4)
- [ ] Visible focus indicators (2px ring)
- [ ] Color is not the only indicator (use icons + text)

---

## Sources & References

- Google Fonts: https://fonts.google.com/knowledge
- U.S. Web Design System: https://designsystem.digital.gov
- WCAG Guidelines: https://www.w3.org/WAI/WCAG21/quickref/
- FontPair: https://www.fontpair.co
- Tailwind CSS: https://tailwindcss.com/docs

---

**Last Updated**: December 2025
**Version**: 1.0
