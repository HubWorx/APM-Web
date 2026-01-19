# Website Design Specification

## Design Theme: Feature Badge Display

This specification describes a modern product feature showcase design inspired by premium product packaging aesthetics.

---

## Color Palette

| Element | Color | Hex Code |
|---------|-------|----------|
| Background | Dark Black | `#1a1a1a` or `#0d0d0d` |
| Primary Accent | Golden Yellow | `#d4a017` or `#e6b422` |
| Secondary Accent | Warm Gold | `#c9a227` |
| Text Primary | Golden Yellow | `#d4a017` |
| Text Secondary | Off-White | `#f5f5f5` |
| Badge Border | Golden Yellow | `#d4a017` |

---

## Typography

- **Headings**: Bold, sans-serif (e.g., Inter, Roboto, or system-ui)
- **Feature Labels**: Bold uppercase for emphasis
- **Descriptions**: Regular weight, smaller size
- **Numbers/Stats**: Extra bold, large size for impact

---

## Layout Components

### 1. Feature Badges

Rounded rectangle containers with:
- **Border**: 2-3px solid golden yellow outline
- **Background**: Transparent or slight dark tint
- **Padding**: 12-20px
- **Border Radius**: 8-12px
- **Content**: Icon + Text combination

### 2. Badge Variations

#### Standard Badge (Rectangular)
```
+------------------+
|  FEATURE NAME    |
|     [icon]       |
+------------------+
```

#### Arch/Banner Badge
```
    .-----------.
   /  SUPER-BRIGHT  \
  |  ANTI-GLARE     |
  |    DISPLAY      |
   \_______________/
```

#### Circular Badge
```
    .-----.
   /       \
  |   14+   |
  | HOUR    |
  | BATTERY |
   \_______/
```

#### Pill Badge
```
+--------+
| USB-C  |
+--------+
```

---

## Feature Display Examples

### IP Rating Badge
- **Icon**: Cloud with rain/water drops
- **Text**: "IP" on top, "67" below (large)
- **Style**: Outlined rectangle

### Display Quality Badge
- **Header Text**: "SUPER-BRIGHT" (curved/arched)
- **Main Text**: "ANTI-GLARE DISPLAY"
- **Icon**: Sun symbol
- **Style**: Arch-top banner shape

### Connectivity Badge
- **Text**: "USB-C"
- **Style**: Simple pill/rounded rectangle

### Button Feature Badge
- **Header Text**: "GLOVE-FRIENDLY" (curved around icon)
- **Main Text**: "BUTTONS"
- **Icon**: Hand/finger pressing button
- **Style**: Circular with text wrap

### Battery Badge
- **Main Text**: "14+" (large)
- **Sub Text**: "HOUR BATTERY"
- **Style**: Oval/ellipse shape

### Alert Feature
- **Icon**: Three LED indicator dots
- **Text**: "alert" and "LED"
- **Style**: Minimal, icon-focused

### Speed/Gauge Badge
- **Icon**: Semicircular gauge with indicator
- **Number**: "30" in circle
- **Text**: "speedo"
- **Style**: Gauge graphic with text

### Clock Badge
- **Text**: "CLOCK"
- **Style**: Simple outlined rectangle

---

## CSS Implementation Guidelines

```css
/* Base theme */
:root {
  --bg-dark: #0d0d0d;
  --accent-gold: #d4a017;
  --accent-gold-light: #e6b422;
  --text-light: #f5f5f5;
}

/* Feature badge base */
.feature-badge {
  border: 2px solid var(--accent-gold);
  border-radius: 10px;
  padding: 16px 24px;
  background: transparent;
  color: var(--accent-gold);
  display: inline-flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

/* Badge text styles */
.badge-title {
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.badge-value {
  font-size: 2.5rem;
  font-weight: 800;
}

.badge-subtitle {
  font-size: 0.75rem;
  text-transform: uppercase;
}

/* Icon styling */
.badge-icon {
  width: 32px;
  height: 32px;
  stroke: var(--accent-gold);
  fill: none;
  stroke-width: 2;
}
```

---

## Grid Layout

Features should be arranged in a responsive grid:
- **Desktop**: 3-4 columns
- **Tablet**: 2-3 columns
- **Mobile**: 1-2 columns

```css
.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 20px;
  padding: 40px;
  background: var(--bg-dark);
}
```

---

## Animation & Interactions

- **Hover**: Subtle glow effect on badges
- **Focus**: Increased border brightness
- **Transition**: Smooth 0.2s ease for all interactive states

```css
.feature-badge:hover {
  box-shadow: 0 0 20px rgba(212, 160, 23, 0.3);
  border-color: var(--accent-gold-light);
}
```

---

## Icon Requirements

All icons should be:
- Line/stroke style (not filled)
- 2px stroke width
- Golden yellow color matching accent
- SVG format for scalability

### Required Icons:
1. Cloud with rain drops (IP/water rating)
2. Sun with rays (brightness/display)
3. Hand/finger pointing (touch/buttons)
4. Battery outline (power)
5. LED dots pattern (alerts)
6. Gauge/speedometer (speed)
7. Clock face (time)
8. USB-C connector (connectivity)

---

## Responsive Breakpoints

| Breakpoint | Width | Columns |
|------------|-------|---------|
| Mobile | < 640px | 2 |
| Tablet | 640-1024px | 3 |
| Desktop | > 1024px | 4 |

---

## Accessibility

- Minimum contrast ratio: 4.5:1 (gold on black exceeds this)
- All icons must have aria-labels
- Focus states must be visible
- Text should be readable at 200% zoom

---

## Example HTML Structure

```html
<section class="features-section">
  <div class="features-grid">

    <div class="feature-badge badge-rect">
      <span class="badge-title">IP</span>
      <svg class="badge-icon"><!-- cloud icon --></svg>
      <span class="badge-value">67</span>
    </div>

    <div class="feature-badge badge-arch">
      <span class="badge-header">SUPER-BRIGHT</span>
      <div class="badge-content">
        <span>ANTI</span>
        <svg class="badge-icon"><!-- sun icon --></svg>
        <span>GLARE</span>
      </div>
      <span class="badge-subtitle">DISPLAY</span>
    </div>

    <div class="feature-badge badge-pill">
      <span class="badge-title">USB-C</span>
    </div>

    <div class="feature-badge badge-circle">
      <span class="badge-header">GLOVE-FRIENDLY</span>
      <svg class="badge-icon"><!-- hand icon --></svg>
      <span class="badge-subtitle">BUTTONS</span>
    </div>

    <div class="feature-badge badge-oval">
      <span class="badge-value">14<sup>+</sup></span>
      <span class="badge-subtitle">HOUR BATTERY</span>
    </div>

    <div class="feature-badge badge-minimal">
      <span class="badge-label">alert</span>
      <svg class="badge-icon"><!-- LED dots --></svg>
      <span class="badge-title">LED</span>
    </div>

    <div class="feature-badge badge-gauge">
      <svg class="badge-icon"><!-- speedometer --></svg>
      <span class="badge-title">speedo</span>
    </div>

    <div class="feature-badge badge-rect">
      <span class="badge-title">CLOCK</span>
    </div>

  </div>
</section>
```

---

## Design Principles

1. **Contrast**: High contrast between dark background and gold accents
2. **Hierarchy**: Important features use larger badges/text
3. **Balance**: Asymmetric but visually balanced layout
4. **Clarity**: Each feature clearly identifiable at a glance
5. **Premium Feel**: Gold on black conveys quality and sophistication
