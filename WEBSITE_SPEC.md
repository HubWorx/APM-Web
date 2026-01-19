# APM Value Calculator - Complete Specification

## Overview

**Product Name:** AI-Powered APM Value Calculator
**Purpose:** Interactive web application that guides users through understanding different Asset Performance Management (APM) approaches and calculates ROI for their organization
**Target Audience:** Oil & Gas and Power Generation industry decision-makers
**Last Updated:** 2026-01-19

---

## Design Theme: Feature Badge Display

This specification describes a modern product feature showcase design inspired by premium product packaging aesthetics with an orange-on-black color scheme.

---

## Color Palette

| Element | Color | Hex Code |
|---------|-------|----------|
| Background | Dark Black | `#0a0a0a` |
| Surface | Dark Surface | `#141414` |
| Card | Dark Card | `#1e1e1e` |
| Primary Accent | Vibrant Orange | `#ff6b00` |
| Secondary Accent | Light Orange | `#ff8533` |
| Dark Accent | Dark Orange | `#cc5500` |
| Text Primary | White | `#ffffff` |
| Text Secondary | Gray 300 | `#d1d5db` |
| Text Muted | Gray 400/500 | `#9ca3af` / `#6b7280` |
| Badge Border | Orange | `#ff6b00` |

### Chart Data Colors (Multi-Color)

| Category | Color | Hex Code |
|----------|-------|----------|
| Asset Strategy | Red | `#ef4444` |
| Risk & Performance | Orange | `#f97316` |
| Planning & Optimization | Yellow | `#eab308` |
| Equipment Health | Green | `#22c55e` |
| Predictive Maintenance | Blue | `#3b82f6` |

### Approach Colors

| Approach | Background | Border |
|----------|------------|--------|
| Traditional | Red tones | `#fef2f2`, `#dc2626` |
| Health-Centric | Blue/Green tones | `#dbeafe`, `#16a34a` |
| Holistic | Purple tones | `#faf5ff`, `#9333ea` |

---

## Typography

### Font Rendering
```css
* {
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-rendering: optimizeLegibility;
}
```

### Text Hierarchy

| Element | Mobile | Desktop | Weight |
|---------|--------|---------|--------|
| H1 | `text-3xl` | `text-5xl` | Bold |
| H2 | `text-2xl` | `text-4xl` | Bold |
| H3 | `text-xl` | `text-2xl` | Bold |
| H4 | `text-lg` | `text-xl` | Bold |
| Body | `text-sm` | `text-base` | Normal |
| Small | `text-xs` | `text-sm` | Normal |

### Text Colors
- **Headings**: White (`text-white`)
- **Feature Labels**: Orange (`text-orange`)
- **Descriptions**: Gray 300-400 (`text-gray-300`, `text-gray-400`)
- **Muted**: Gray 500 (`text-gray-500`)

---

## Layout Components

### Feature Badges

Rounded rectangle containers with:
- **Border**: 2px solid orange (`#ff6b00`)
- **Background**: Dark surface (`#141414`) or dark card (`#1e1e1e`)
- **Padding**: `p-4 md:p-6` or `p-6 md:p-8`
- **Border Radius**: 12px
- **Transition**: 0.2s ease

```css
.feature-badge {
    border: 2px solid #ff6b00;
    border-radius: 12px;
    transition: all 0.2s ease;
}
.feature-badge:hover {
    box-shadow: 0 0 20px rgba(255, 107, 0, 0.3);
    border-color: #ff8533;
}
```

### Badge Variations

| Type | Border Radius | Use Case |
|------|---------------|----------|
| Standard | `12px` | Cards, sections |
| Pill | `50px` | Buttons, tags |
| Circular | `50%` | Icons, small badges |

---

## Website Flow

### 6-Step Journey

1. **Industry Selection** - User chooses their industry
2. **Traditional ISO 55000 Approach** - Shows old methodology (4-5 years)
3. **Disruptive Technology Companies** - Showcases AI-powered APM vendors
4. **Holistic Asset Intelligence** - Presents combined approach (18 months)
5. **Comparison** - Side-by-side charts and case studies
6. **ROI Calculator** - Personalized financial impact calculation

---

## Step-by-Step Specifications

### Step 1: Industry Selection

**Visual Elements:**
- Title: "APM Value Realization Journey" (white, bold)
- Subtitle: "Choose your industry to begin" (gray-300)
- Two large button cards in 2-column grid

**Industry Buttons:**

| Industry | Icon | Description | Style |
|----------|------|-------------|-------|
| Oil & Gas | SVG layers icon | "ROCE analysis for upstream, midstream, downstream" | Orange border badge |
| Power Generation | SVG lightning icon | "Availability and O&M cost per MWh analysis" | Orange border badge |

**Interactions:**
- Hover: Box shadow glow, border lightens
- Click: Navigate to Step 2 with selected industry data

---

### Step 2: Traditional ISO 55000 Approach

**Header:**
- Industry badge (orange border, white text, pill shape)
- Title: "Traditional ISO 55000 Approach" (white)

**Content Card:**
- Border: 2px orange
- Warning banner: Orange left border, "The Old Way: Framework-first, technology-last"

**Chart 1: Traditional ROCE Progress**
- Type: Stacked bar chart
- X-axis: Tier 1, Tier 2, Tier 3
- Y-axis: ROCE Improvement (%)
- Colors: Red, Orange, Yellow, Green, Blue (distinct per category)
- Legend: Displayed at bottom (white text)
- Height: 280px

**Key Metrics (3-column grid):**

| Metric | Value | Label |
|--------|-------|-------|
| Timeline | 4-5 | Years |
| ROCE Impact | +5.7% / +16.4% | Impact |
| First 2 Years | ~0 | Value |

**CTA Button:**
- Text: "What Changed?"
- Style: Orange border pill, white text, hover fills orange

---

### Step 3: Disruptive Technology Companies

**Header:**
- Title: "The Last Decade Changed Everything" (white)
- Subtitle: "Technology disruption enabling health-centric APM" (gray-300)

**Technology Feature Badges (2x2 or 4-column grid):**

| Technology | Icon | Metric |
|------------|------|--------|
| Cloud | Cloud SVG | Deploy in Days |
| IoT | Chip SVG | 90% Cost Reduction |
| AI & ML | Lightbulb SVG | 87% Accuracy |
| Big Data | Database SVG | Real-Time Insights |

**Company Cards (6 total, 2-column grid):**

| Company | Impact | Metric | Description |
|---------|--------|--------|-------------|
| Databricks | 10x Faster | Data processing | Unified data lakehouse platform |
| Augury | 70% Reduction | Unplanned downtime | AI-powered machine health |
| Uptake | 50M Hours | Prevented downtime | Industrial AI platform |
| C3 AI | 3-6 Months | Time to value | Enterprise AI suite |
| Samsara | 25% Decrease | Maintenance costs | Connected operations cloud |
| Presenso | 95% Accuracy | 30+ day prediction | Self-learning AI |

**Why Disruptors Win (3-column):**
1. Rapid Deployment - Cloud-native, weeks not years
2. AI-First Approach - Built on ML from ground up
3. Pay-as-You-Grow - Subscription models

**Vendor Innovation Section:**
- GE Vernova: SmartSignal AI - Zero breakdowns at Total EP
- AspenTech: Aspen Mtell - OCP Ecuador +20% uptime
- IBM Maximo: 87% failure prediction accuracy

**CTA Button:**
- Text: "See Health-Centric Approach"
- Style: Orange border pill

---

### Step 4: Holistic Asset Intelligence

**Header:**
- Title: "Holistic Asset Intelligence" (white)
- Subtitle: "Combining strategic frameworks with cutting-edge AI" (gray-300)

**The Ultimate Approach (2-column):**

**Strategic Foundation:**
- ISO 55000 governance framework
- Clear asset strategy alignment
- Risk-based planning processes
- Stakeholder buy-in and change management

**AI-Powered Execution:**
- Real-time health monitoring (Augury, Uptake)
- Predictive maintenance (Presenso, C3 AI)
- Data lakehouse analytics (Databricks)
- Connected operations (Samsara)

**The Synergy Effect (3-column):**
1. Better Decisions - Strategic clarity meets real-time data
2. Faster Results - Framework accelerates AI deployment
3. Maximum Value - 15-20% higher ROCE than either alone

**Implementation Roadmap (4-phase):**
| Phase | Timeline | Activity |
|-------|----------|----------|
| 1 | Month 1-3 | Quick wins with AI tools on critical assets |
| 2 | Month 4-8 | Deploy governance framework in parallel |
| 3 | Month 9-18 | Scale AI across asset portfolio |
| 4 | Month 18+ | Continuous optimization and expansion |

**CTA Button:**
- Text: "Compare All Approaches"

---

### Step 5: Comparison

**Header:**
- Title: "Compare the Approaches" (white)

**Comparison Charts (2-column grid):**

| Chart | Title | ROCE | Timeline |
|-------|-------|------|----------|
| Chart 2 | Traditional | +5.7% / +16.4% | 4-5 years |
| Chart 3 | Health-Centric | +12.2% / +29.8% | 3 years |

**Case Studies (3-column grid):**

| Company | Vendor | Result |
|---------|--------|--------|
| OQ (Oman) | GE Vernova APM | $59M Saved |
| OCP Ecuador | AspenTech | +20% Uptime |
| Total EP | GE Vernova | Zero Breakdowns |

**CTA Button:**
- Text: "Calculate Your ROI"

---

### Step 6: ROI Calculator

**Header:**
- Title: "Calculate Your ROI" (white)

**Input Form (2x2 grid):**

| Field | Type | Placeholder |
|-------|------|-------------|
| Revenue ($M) | Number | 1000 |
| Capital ($M) | Number | 500 |
| Profit ($M) | Number | 100 |
| Maintenance ($M) | Number | 50 |

**Input Styling:**
```css
input[type="number"] {
    background: #1e1e1e;
    border: 2px solid #ff6b00;
    color: #ffffff;
}
input::placeholder { color: #888888; }
input:focus { box-shadow: 0 0 10px rgba(255, 107, 0, 0.3); }
```

**Calculate Button:**
- Text: "Calculate Results"
- Style: Orange background, black text, pill shape

**Results Display (3-column):**

| Approach | Timeline | Maint Savings |
|----------|----------|---------------|
| Traditional | 5 Years | 15% |
| Health-Centric | 3 Years | 30% |
| Holistic | 18 Months | 40% |

**Advantage Banner:**
- Background: Orange
- Text: Black
- Shows difference between Holistic and Traditional

---

## Data Models

### Industry ROCE Data

```javascript
const DATA = {
    oilgas: {
        trad: {
            strategy: [0.3, 0.3, 0.3],
            risk: [0.2, 0.5, 0.5],
            planning: [0, 0.4, 0.6],
            health: [0, 0.6, 1.2],
            predictive: [0, 0, 0.8],
            total: 5.7
        },
        health: {
            health: [1.5, 1.5, 1.5],
            predictive: [1.0, 1.2, 1.2],
            risk: [0.3, 0.8, 0.8],
            planning: [0, 0.7, 1.0],
            strategy: [0, 0.2, 0.5],
            total: 12.2
        },
        holistic: {
            health: [1.8, 1.8, 1.8],
            predictive: [1.5, 1.8, 1.8],
            risk: [0.5, 1.2, 1.2],
            planning: [0.3, 1.0, 1.4],
            strategy: [0.4, 0.5, 0.8],
            total: 15.9
        }
    },
    powergen: {
        trad: {
            strategy: [1.2, 1.2, 1.2],
            risk: [0.8, 1.5, 1.5],
            planning: [0, 1.0, 1.5],
            health: [0, 1.5, 3.0],
            predictive: [0, 0, 2.0],
            total: 16.4
        },
        health: {
            health: [3.5, 3.5, 3.5],
            predictive: [2.5, 3.0, 3.0],
            risk: [0.8, 2.0, 2.0],
            planning: [0, 1.8, 2.5],
            strategy: [0, 0.5, 1.2],
            total: 29.8
        },
        holistic: {
            health: [4.2, 4.2, 4.2],
            predictive: [3.5, 4.0, 4.0],
            risk: [1.2, 2.8, 2.8],
            planning: [0.5, 2.5, 3.5],
            strategy: [0.8, 1.0, 1.8],
            total: 38.3
        }
    }
};
```

### Maintenance Savings Constants

```javascript
const MAINTENANCE_SAVINGS = {
    TRADITIONAL: 0.15,      // 15%
    HEALTH_CENTRIC: 0.30,   // 30%
    HOLISTIC: 0.40          // 40%
};
```

---

## Calculation Formulas

### Traditional Approach
```
Profit Gain = Profit × (Traditional ROCE% ÷ 100)
Maintenance Savings = Maintenance × 0.15
Total Value = Profit Gain + Maintenance Savings
```

### Health-Centric Approach
```
Profit Gain = Profit × (Health-Centric ROCE% ÷ 100)
Maintenance Savings = Maintenance × 0.30
Total Value = Profit Gain + Maintenance Savings
```

### Holistic Approach
```
Profit Gain = Profit × (Holistic ROCE% ÷ 100)
Maintenance Savings = Maintenance × 0.40
Total Value = Profit Gain + Maintenance Savings
```

### Holistic Advantage
```
Advantage = Holistic Total Value - Traditional Total Value
```

---

## Responsive Design

### Breakpoints

| Breakpoint | Width | Description |
|------------|-------|-------------|
| Base | < 640px | Mobile, single column |
| sm | 640px+ | 2-column grids |
| md | 768px+ | Some 3-column grids |
| lg | 1024px+ | Full layouts |

### Typography Scaling

| Element | Mobile | Desktop |
|---------|--------|---------|
| H1 | `text-3xl` | `md:text-5xl` |
| H2 | `text-2xl` | `md:text-4xl` |
| H3 | `text-lg` | `md:text-xl` |
| Body | `text-sm` | `md:text-base` |
| Buttons | `text-base` | `md:text-lg` |

### Padding Scaling

| Element | Mobile | Desktop |
|---------|--------|---------|
| Cards | `p-4` | `md:p-6` |
| Sections | `p-6` | `md:p-8` or `md:p-12` |
| Buttons | `px-6 py-2` | `md:px-8 md:py-3` |
| Gaps | `gap-3` or `gap-4` | `md:gap-6` |

### Grid Layouts

| Component | Mobile | Tablet | Desktop |
|-----------|--------|--------|---------|
| Industry buttons | 1 col | 2 col | 2 col |
| Tech badges | 2 col | 4 col | 4 col |
| Company cards | 1 col | 2 col | 2 col |
| Metric badges | 3 col | 3 col | 3 col |
| Calculator inputs | 2 col | 2 col | 2 col |
| Results | 1 col | 2 col | 3 col |
| Case studies | 1 col | 2 col | 3 col |
| Charts | 1 col | 1 col | 2 col |

---

## Chart Specifications

### Common Configuration

```javascript
Chart.defaults.color = '#ffffff';
Chart.defaults.borderColor = '#333333';
```

### Chart Options

| Property | Value |
|----------|-------|
| Type | Stacked bar |
| Responsive | true |
| Maintain Aspect Ratio | false |
| Grid Color | `#333333` |
| Tick Color | `#ffffff` |
| Legend Color | `#ffffff` |

### Chart Colors

```javascript
const colors = {
    strategy: '#ef4444',    // Red
    risk: '#f97316',        // Orange
    planning: '#eab308',    // Yellow
    health: '#22c55e',      // Green
    predictive: '#3b82f6'   // Blue
};
```

---

## Accessibility Features

### WCAG Compliance
- Semantic HTML with proper heading hierarchy
- ARIA labels on interactive elements
- Keyboard navigation support
- Screen reader compatible charts
- Minimum 4.5:1 contrast ratio (orange on black exceeds this)
- Focus states visible on all interactive elements

### Implementation
```html
<nav role="navigation" aria-label="Main navigation">
<button aria-label="Select Oil & Gas industry">
<input aria-required="true" aria-label="Revenue in millions">
<canvas role="img" aria-label="ROCE improvement chart">
```

---

## Security Features

- External links use `rel="noopener noreferrer"`
- CDN resources use HTTPS
- Client-side input validation
- No sensitive data storage

---

## Technical Stack

| Component | Technology |
|-----------|------------|
| Markup | HTML5 semantic |
| Styling | Tailwind CSS (CDN) |
| Charts | Chart.js v4.4.1 |
| Scripts | Vanilla ES6+ |
| Build | None required |

---

## Icon Requirements

All icons should be:
- SVG format for scalability
- Line/stroke style (not filled)
- 2px stroke width
- Orange color (`#ff6b00`) or currentColor
- Sized with Tailwind (`w-5 h-5` to `w-8 h-8`)

### Required Icons
1. Layers/stack (Oil & Gas)
2. Lightning bolt (Power Generation)
3. Cloud (Cloud computing)
4. Chip/processor (IoT)
5. Lightbulb (AI & ML)
6. Database/cylinder (Big Data)

---

## Animation & Interactions

| Element | Trigger | Effect |
|---------|---------|--------|
| Feature badges | Hover | Box shadow glow, border lightens |
| Buttons | Hover | Background fills orange, text turns black |
| Inputs | Focus | Orange glow shadow |
| Cards | Hover | Background darkens slightly |

```css
.feature-badge:hover {
    box-shadow: 0 0 20px rgba(255, 107, 0, 0.3);
    border-color: #ff8533;
}
button:hover {
    background: #ff6b00;
    color: #000000;
}
```

---

## Navigation Logic

### State Management
```javascript
let currentIndustry = null;  // 'oilgas' or 'powergen'
let charts = {};              // Store chart instances
```

### Step Transitions
1. `selectIndustry(industry)` - Step 1 → 2
2. `goToStep3()` - Step 2 → 3
3. `goToStep4()` - Step 3 → 4
4. `goToStep5()` - Step 4 → 5
5. `goToStep6()` - Step 5 → 6
6. `calculate()` - Compute and display results
7. `location.reload()` - Restart

### Helper Functions
- `hideAll()` - Hides all 6 steps
- `drawChart(canvasId, data, showLegend)` - Renders Chart.js
- `window.scrollTo(0,0)` - Scroll to top on transition

---

## Error Handling

### Input Validation
```javascript
if (rev <= 0 || cap <= 0 || prof <= 0 || maint <= 0) {
    alert('Please enter valid positive values.');
    return;
}
```

### Chart Rendering
```javascript
if (!canvas) return;
if (charts[canvasId]) charts[canvasId].destroy();
```

---

## File Structure

```
/home/user/APM-Web/
├── index.html           # Main application file
├── WEBSITE_SPEC.md      # This specification document
└── .git/                # Git repository
```

---

## Deployment

### Requirements
- Static web hosting (no server required)
- HTTPS recommended for CDN security
- No build process needed

### Hosting Options
- GitHub Pages
- Netlify
- Vercel
- AWS S3 + CloudFront
- Any static web host

---

## Design Principles

1. **Contrast**: High contrast between dark background and orange accents
2. **Hierarchy**: Important features use larger text and prominent badges
3. **Clarity**: White text ensures readability, orange for emphasis
4. **Sharpness**: Antialiased text rendering for crisp typography
5. **Premium Feel**: Orange on black conveys energy and sophistication
6. **Consistency**: Same badge styling throughout all steps

---

## Testing Checklist

- [ ] All 6 steps load correctly
- [ ] Charts render with multi-color bars
- [ ] Calculator produces accurate results
- [ ] Text fits properly on all buttons
- [ ] Responsive design works on mobile/tablet/desktop
- [ ] All navigation buttons work
- [ ] Input validation functions
- [ ] Text is sharp and readable
- [ ] External links open in new tabs
- [ ] No console errors

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| v1.0 | 2026-01-18 | Initial release |
| v1.1 | 2026-01-19 | Orange/black theme, white text, multi-color charts |

---

**End of Specification Document**
