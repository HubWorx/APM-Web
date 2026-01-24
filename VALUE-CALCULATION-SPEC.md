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

## Supporting Evidence: Traditional Approach (ISO 55000)

The Traditional approach assumptions are supported by documented ISO 55001 implementations:

### Utility Industry Case Studies

| Organization | Benefits Achieved | Source |
|--------------|-------------------|--------|
| [Scottish Water](https://committee.iso.org/files/live/sites/tc251/files/stories/BSI-ISO-55001-Case-Study-Scottish-Water-UK-EN.pdf) | Improved asset efficiency, enhanced customer service, broke down departmental silos | BSI Case Study |
| [Palm Beach County Water Utilities](https://committee.iso.org/sites/tc251/social-links/resources/case-studies.html) | People-led asset management framework implementation | ISO TC251 |
| [Gladstone Area Water Board](https://committee.iso.org/sites/tc251/social-links/resources/case-studies.html) | Sound asset practices contributing to water price setting | ISO TC251 |
| [Lansing Board of Water & Light](https://committee.iso.org/sites/tc251/social-links/resources/case-studies.html) | Demonstrated municipal utility benefits | ISO TC251 |
| [Energinet](https://committee.iso.org/sites/tc251/social-links/resources/case-studies.html) | Power utility asset management improvements | ISO TC251 |

### Documented ISO 55001 Benefits

According to [Bureau Veritas](https://certification.bureauveritas.com/asset-management-system-iso-55001-certification) and [NQA](https://www.nqa.com/en-us/certification/standards/iso-55001):
- Lower costs and maximized ROI throughout asset lifecycle
- Extended asset life through reliability-centered maintenance
- Reduced operational costs
- Better planning for major capital expenditures
- Demonstrated compliance to regulators and stakeholders

### Why Traditional Takes Longer (5 Years)

[U.S. utilities research](https://breakingenergy.com/2016/07/28/u-s-utilities-weigh-the-cost-and-benefit-of-iso-55001certification/) indicates that ISO 55001 certification requires:
- Comprehensive governance framework development
- Cross-departmental alignment and cultural change
- Stakeholder buy-in processes
- Independent audit and certification cycles

---

## Supporting Evidence: Health-Centric Approach (AI/ML)

The Health-Centric approach assumptions are supported by documented AI/predictive maintenance implementations:

### Industry Research & Benchmarks

| Metric | Finding | Source |
|--------|---------|--------|
| Downtime Reduction | 35-45% reduction | [Deloitte Research](https://www.netguru.com/blog/ai-predictive-maintenance) |
| Unexpected Breakdowns | 70-75% elimination | [Deloitte Research](https://www.netguru.com/blog/ai-predictive-maintenance) |
| Maintenance Cost Reduction | 25-30% reduction | [Deloitte Research](https://www.netguru.com/blog/ai-predictive-maintenance) |
| Prediction Accuracy | Up to 90% | IBM, 2024 |
| Typical ROI Timeline | 12-24 months | [Industry Analysis](https://www.netguru.com/blog/ai-predictive-maintenance) |

### Specific Case Studies

| Company | Technology | Results | Source |
|---------|------------|---------|--------|
| **Aker BP** | Cognite Data Fusion | $6.5M OpEx savings, 1,300 hours saved, 30% maintenance reduction, 70% fewer shutdowns, 40% increased pump availability | [Cognite](https://www.cognite.com/en/resources/customer-stories/dataops-oil-gas-siemens-condition-monitoring) |
| **Aker BP** | Cognite ML | $6M annual savings from oil-in-water monitoring alone | [Cognite](https://www.cognite.com/en/resources/customer-stories/dataops-oil-gas-hybrid-machine-learning) |
| **Aker BP** | Cognite DataOps | 100,000 metric tons CO2 reduction/year at Skarv field | [Cognite](https://www.cognite.com/en/resources/customer-stories/dataops-oil-gas-reducing-co2-emissions) |
| **Shell** | C3 AI | Monitored 10,000+ assets, 20B data points/week, $2M saved from 2 prevented failures | [Think AI Corp](https://thinkaicorp.com/case-study-cutting-machine-downtime-with-predictive-maintenance-and-ai/) |
| **Fortune 500 Manufacturer** | AI Predictive Maintenance | 45% downtime reduction, $2.8M annual savings | [Netguru](https://www.netguru.com/blog/ai-predictive-maintenance) |
| **Midwest Steel Manufacturer** | IoT + ML | 30% downtime reduction, $850K annual savings, 11-month ROI, 31% OEE improvement | [OxMaint](https://oxmaint.com/case-study/post/predictive-maintenance-downtime-reduction) |
| **Semiconductor Fab** | AI Vibration Monitoring | 72% decrease in unscheduled downtime | [Ademero](https://www.ademero.com/ai-resources/case-studies/manufacturing-predictive-maintenance) |
| **Chevron** | Seeq Analytics | Data analysis reduced from 4 months to 30 minutes | [Microsoft Case Study](https://partner.microsoft.com/en-us/case-studies/seeq) |

### Machine Health Platform Results

[Augury's 2024 Machine Health Report](https://www.businesswire.com/news/home/20240807908808/en/Augurys-2024-Machine-Health-Is-Business-Health-Report-Outlines-the-Current-State-of-Asset-Maintenance-and-Its-Top-Roadblocks) and Forrester TEI Study findings:

| Metric | Result |
|--------|--------|
| ROI | 310% with <6 month payback |
| Customer ROI Range | 3-10x, often 5-20x |
| Pilot Results | 2.5x ROI in 8 months on 40-machine pilot |

### Why Health-Centric is Faster (3 Years)

According to [MIT Sloan Management Review](https://sloanreview.mit.edu/article/a-maintenance-revolution-reducing-downtime-with-ai-tools/):
- Pre-trained industry-specific AI models accelerate deployment
- Cloud-based analytics eliminate IT infrastructure overhead
- Sensor costs have dropped 60% since 2020
- Average ROI timeline has shrunk from 18 months to <6 months

---

## Comparison Summary

| Factor | Traditional (ISO 55000) | Health-Centric (AI/ML) |
|--------|------------------------|------------------------|
| **Time to Value** | 3-5 years | 6-18 months |
| **Primary Focus** | Governance & Framework | Technology & Data |
| **Maintenance Savings** | 15% (process improvement) | 25-30% (predictive) |
| **Downtime Impact** | Incremental improvement | 35-70% reduction |
| **Best For** | Regulatory compliance, long-term governance | Quick wins, operational efficiency |
| **Risk** | Slow ROI, change fatigue | Data quality, legacy system integration |

---

## Code Reference

The calculation logic is implemented in `index.html`:
- Data constants: Lines 1536-1595
- Calculate function: Lines 1789-1900+

Key variables:
- `DATA[industry].approach.total` - ROCE improvement percentages
- `MAINTENANCE_SAVINGS` - Savings factors by approach
- `DOWNTIME_FACTORS` - Revenue percentage for downtime value
