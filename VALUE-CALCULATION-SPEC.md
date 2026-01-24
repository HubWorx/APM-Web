# APM Value Calculator - Calculation Specification

This document explains how the ROI/Value calculations work in the APM Value Calculator.

## Overview

The calculator estimates annual value generation from three APM (Asset Performance Management) approaches:
1. **Traditional** - ISO 55000 framework-first approach (5-year implementation)
2. **Health-Centric** - AI/ML technology-first approach (3-year implementation)
3. **Holistic** - Combined strategic framework + AI approach (3-year implementation)

---

## User Inputs

| Input | Description | Unit |
|-------|-------------|------|
| Annual Revenue | Total annual revenue from all business operations | $M |
| Capital Employed | Total assets minus current liabilities | $M |
| Operating Profit | EBIT - Earnings before interest and taxes | $M |
| Operating Expense | Total annual operating costs (excluding COGS) | $M |
| Maintenance % | Percentage of OpEx allocated to maintenance (20-60%) | % |

### Derived Input
```
Maintenance Spend = Operating Expense × (Maintenance % / 100)
```

---

## Value Components

The total annual value for each approach is calculated from three components:

### 1. Operating Profit Gains
Based on ROCE (Return on Capital Employed) improvement percentages.

```
Profit Gain = Operating Profit × (ROCE Improvement % / 100)
```

### 2. Maintenance Savings
Percentage reduction in maintenance spend.

| Approach | Savings Factor |
|----------|---------------|
| Traditional | 15% |
| Health-Centric | 30% |
| Holistic | 40% |

```
Maintenance Savings = Maintenance Spend × Savings Factor
```

### 3. Downtime Reduction Value
Value recovered from reduced unplanned downtime, expressed as percentage of revenue.

| Approach | Downtime Factor |
|----------|----------------|
| Traditional | 0.5% of revenue |
| Health-Centric | 1.5% of revenue |
| Holistic | 2.5% of revenue |

```
Downtime Value = Annual Revenue × Downtime Factor
```

---

## Total Value Calculation

```
Annual Value = Profit Gain + Maintenance Savings + Downtime Value
```

For multi-year projections:
- **Traditional**: Value realized in years 3-5 (slower ramp-up)
- **Health-Centric**: Value realized over 3 years
- **Holistic**: Value realized over 3 years (faster time-to-value)

---

## Industry-Specific ROCE Data

### Oil & Gas Industry

| Approach | ROCE Improvement | Implementation |
|----------|-----------------|----------------|
| Traditional | +5.7% | 5 years |
| Health-Centric | +12.2% | 3 years |
| Holistic | +15.9% | 3 years |

**ROCE Component Breakdown (Oil & Gas):**

Traditional approach builds value over 5 years through:
- Asset Strategy: 0.3% → 0.3% → 0.3%
- Risk Management: 0.2% → 0.5% → 0.5%
- Planning & Scheduling: 0% → 0.4% → 0.6%
- Asset Health: 0% → 0.6% → 1.2%
- Predictive Maintenance: 0% → 0% → 0.8%

Health-Centric approach prioritizes technology:
- Asset Health: 1.5% → 1.5% → 1.5%
- Predictive Maintenance: 1.0% → 1.2% → 1.2%
- Risk Management: 0.3% → 0.8% → 0.8%
- Planning & Scheduling: 0% → 0.7% → 1.0%
- Asset Strategy: 0% → 0.2% → 0.5%

Holistic approach combines both:
- Asset Health: 1.8% → 1.8% → 1.8%
- Predictive Maintenance: 1.5% → 1.8% → 1.8%
- Risk Management: 0.5% → 1.2% → 1.2%
- Planning & Scheduling: 0.3% → 1.0% → 1.4%
- Asset Strategy: 0.4% → 0.5% → 0.8%

### Power Generation Industry

| Approach | ROCE Improvement | Implementation |
|----------|-----------------|----------------|
| Traditional | +13.9% | 5 years |
| Health-Centric | +29.8% | 3 years |
| Holistic | +38.3% | 3 years |

**ROCE Component Breakdown (Power Generation):**

Traditional approach (reliability-focused):
- Predictive Maintenance: 3.0% → 3.5% → 3.5%
- Asset Health: 0% → 0.5% → 1.0%
- Risk Management: 0% → 0.5% → 1.0%
- Planning & Scheduling: 0% → 0.2% → 0.5%
- Asset Strategy: 0% → 0% → 0.2%

Health-Centric approach:
- Asset Health: 3.5% → 3.5% → 3.5%
- Predictive Maintenance: 2.5% → 3.0% → 3.0%
- Risk Management: 0.8% → 2.0% → 2.0%
- Planning & Scheduling: 0% → 1.8% → 2.5%
- Asset Strategy: 0% → 0.5% → 1.2%

Holistic approach:
- Asset Health: 4.2% → 4.2% → 4.2%
- Predictive Maintenance: 3.5% → 4.0% → 4.0%
- Risk Management: 1.2% → 2.8% → 2.8%
- Planning & Scheduling: 0.5% → 2.5% → 3.5%
- Asset Strategy: 0.8% → 1.0% → 1.8%

---

## Example Calculation

**Inputs:**
- Annual Revenue: $1,000M
- Capital Employed: $500M
- Operating Profit: $100M
- Operating Expense: $200M
- Maintenance %: 40%

**Derived:**
- Maintenance Spend: $200M × 40% = $80M
- Current ROCE: ($100M / $500M) × 100 = 20%

**Oil & Gas - Traditional Approach:**
```
Profit Gain      = $100M × (5.7 / 100)  = $5.7M
Maintenance Save = $80M × 0.15          = $12.0M
Downtime Value   = $1,000M × 0.005      = $5.0M
─────────────────────────────────────────────────
Annual Total                            = $22.7M
```

**Oil & Gas - Health-Centric Approach:**
```
Profit Gain      = $100M × (12.2 / 100) = $12.2M
Maintenance Save = $80M × 0.30          = $24.0M
Downtime Value   = $1,000M × 0.015      = $15.0M
─────────────────────────────────────────────────
Annual Total                            = $51.2M
```

**Oil & Gas - Holistic Approach:**
```
Profit Gain      = $100M × (15.9 / 100) = $15.9M
Maintenance Save = $80M × 0.40          = $32.0M
Downtime Value   = $1,000M × 0.025      = $25.0M
─────────────────────────────────────────────────
Annual Total                            = $72.9M
```

**Holistic Advantage:** $72.9M - $22.7M = **$50.2M/year** additional value

---

## Key Assumptions

1. **Maintenance as % of OpEx**: Industry typical range is 20-40% for efficient operations, 40-60% for asset-intensive industries

2. **ROCE Improvements**: Based on industry benchmarks and case study data from companies like Aker BP, Chevron, PepsiCo, and BP

3. **Maintenance Savings**: Derived from documented case studies showing 15-40% reductions through various APM approaches

4. **Downtime Reduction**: Based on industry averages for unplanned downtime costs and documented improvements from predictive maintenance implementations

5. **Linear Scaling**: The model assumes linear scaling with company size; actual results may vary based on operational complexity

---

## Code Reference

The calculation logic is implemented in `index.html`:
- Data constants: Lines 1536-1595
- Calculate function: Lines 1789-1900+

Key variables:
- `DATA[industry].approach.total` - ROCE improvement percentages
- `MAINTENANCE_SAVINGS` - Savings factors by approach
- `DOWNTIME_FACTORS` - Revenue percentage for downtime value
