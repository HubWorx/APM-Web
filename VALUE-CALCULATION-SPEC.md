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

## Power Generation Configuration Modifiers

For Power Generation, ROCE values are adjusted based on four configuration parameters selected by the user. This enables more accurate value projections based on the specific business model.

### Configuration Parameters

#### 1. Company Type

| Type | Description | ROCE Modifier |
|------|-------------|---------------|
| **IPP** | Independent Power Producer - own and operate assets, sell competitively | +15% (1.15x) |
| **Utility** | Regulated utility - vertically integrated with T&D | -10% (0.90x) |
| **O&M Contractor** | Operate assets owned by others under contract | -15% (0.85x) |

**Rationale**: IPPs have more upside from operational improvements due to competitive markets. Utilities have regulated returns limiting upside. O&M contractors have fixed-fee structures limiting value capture.

#### 2. Revenue Model

| Model | Description | ROCE Modifier |
|-------|-------------|---------------|
| **Merchant** | Sell into wholesale markets at spot/day-ahead prices | +20% (1.20x) |
| **PPA/Contracted** | Long-term power purchase agreements with fixed pricing | Baseline (1.00x) |
| **Regulated** | Cost-of-service rates set by regulators | -15% (0.85x) |

**Rationale**: Merchant generators have highest sensitivity to availability (high prices during outages). PPA generators have moderate sensitivity (availability penalties). Regulated utilities have cost-plus returns.

#### 3. Asset Type

| Type | Description | ROCE Modifier | Maintenance Complexity |
|------|-------------|---------------|----------------------|
| **Baseload Thermal** | CCGT, Coal, Nuclear - high capacity factor | Baseline (1.00x) | 1.2x |
| **Peaker/Mid-Merit** | Simple cycle GT, Reciprocating engines | +25% (1.25x) | 1.0x |
| **Wind** | Onshore/Offshore wind turbines | +10% (1.10x) | 1.15x |
| **Solar** | Utility-scale photovoltaic | -5% (0.95x) | 0.8x |
| **Hydro** | Run-of-river, Storage hydro | -10% (0.90x) | 0.7x |
| **Battery Storage** | BESS, Grid services | +30% (1.30x) | 0.9x |
| **Mixed Fleet** | Multiple technology types | +5% (1.05x) | 1.1x |

**Rationale**: Peakers and storage have highest value sensitivity to availability (needed during high-price periods). Solar and hydro have lower maintenance intensity and more predictable operations.

#### 4. Region (Fuel Cost Impact)

| Region | Gas Price Benchmark | Fuel Cost Factor |
|--------|--------------------|--------------------|
| **North America** | Henry Hub ($2-4/MMBtu) | 0.9x (lower fuel sensitivity) |
| **Europe** | TTF/NBP ($8-15/MMBtu) | 1.2x (higher fuel sensitivity) |
| **Asia Pacific** | JKM/LNG ($10-18/MMBtu) | 1.3x (highest fuel sensitivity) |
| **Other/Renewable** | N/A | 1.0x (no fuel exposure) |

**Rationale**: Higher fuel costs increase the value of heat rate improvements and efficiency gains. Renewable assets have no fuel cost exposure.

### Modifier Calculation Formula

The final ROCE modifier is calculated as follows:

```
Step 1: Calculate combined modifier (geometric mean)
combinedModifier = (typeModifier × revModifier × assetModifier) ^ (1/3)

Step 2: Apply regional adjustment for fossil assets only
if (assetType == 'baseload' OR assetType == 'peaker'):
    finalModifier = combinedModifier × (2 - regionFuelFactor)
else:
    finalModifier = combinedModifier

Step 3: Apply to base ROCE values
adjustedROCE = baseROCE × finalModifier
```

### Example: IPP Merchant Peaker in North America

**Configuration:**
- Company Type: IPP (1.15x)
- Revenue Model: Merchant (1.20x)
- Asset Type: Peaker (1.25x)
- Region: North America (0.9x fuel factor)

**Calculation:**
```
Combined = (1.15 × 1.20 × 1.25) ^ (1/3) = 1.198
Regional Adjustment = 1.198 × (2 - 0.9) = 1.198 × 1.1 = 1.318

Base Traditional ROCE: +13.9%
Adjusted Traditional ROCE: 13.9% × 1.318 = +18.3%

Base Health-Centric ROCE: +29.8%
Adjusted Health-Centric ROCE: 29.8% × 1.318 = +39.3%

Base Holistic ROCE: +38.3%
Adjusted Holistic ROCE: 38.3% × 1.318 = +50.5%
```

### Configuration Impact Summary

| Configuration | Typical Modifier Range | Best Suited For |
|---------------|----------------------|-----------------|
| IPP + Merchant + Peaker | 1.25-1.35x | Maximum value from availability |
| IPP + PPA + Wind | 1.05-1.15x | Availability penalty avoidance |
| Utility + Regulated + Mixed | 0.75-0.85x | Rate case cost justification |
| O&M + PPA + Baseload | 0.80-0.90x | Contract KPI achievement |

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

### Core Data & Constants
- `DATA` object: Base ROCE values per industry and approach
- `MAINTENANCE_SAVINGS`: Savings factors (0.15, 0.30, 0.40)
- `DOWNTIME_FACTORS`: Revenue percentages (0.005, 0.015, 0.025)

### Power Generation Configuration
- `pgConfig` object: Stores user selections (companyType, revenueModel, assetType, region)
- `PG_MODIFIERS`: ROCE modifiers per configuration option
- `PG_FOCUS_MESSAGES`: Customized value driver messages
- `PG_CONTEXT_MESSAGES`: Customized journey context messages

### Key Functions
- `calculate()`: Main ROI calculation using inputs and ROCE values
- `applyPowerGenConfig()`: Applies configuration modifiers to base ROCE values
- `selectIndustry()`: Sets up industry-specific displays and applies PG config if available
- `getPgContextMessage()`: Returns customized Traditional approach messaging
- `getPgHealthContextMessage()`: Returns customized Health-Centric messaging

### Configured Values Storage
When Power Generation is configured, adjusted values are stored in:
- `DATA.powergen.configuredTrad.total`
- `DATA.powergen.configuredHealth.total`
- `DATA.powergen.configuredHolistic.total`
- `DATA.powergen.configDescription` (display string)
