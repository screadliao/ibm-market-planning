# Phase 2 — WHAT: Segmentation Strategy

Decides WHERE to attack and WITH WHAT. Takes Phase 1 outputs as inputs.

---

## Tool 1: Market Segmentation

**Purpose**: Identify distinct customer/market groups that require different strategies. IBM requires at least two segmentation dimensions — never segment by country alone.

### Segmentation Dimension Selection

Choose dimensions based on product type:

| Product Type | Recommended Dimensions |
|-------------|----------------------|
| Medical device / MedTech | Clinical Application × Market Entry Role |
| B2B SaaS / Enterprise | Industry Vertical × Company Size / Maturity |
| Consumer hardware | Use Case × User Sophistication |
| Industrial / ODM | End Market × Regional Regulatory Complexity |
| Platform / Ecosystem | Workflow Stage × Integration Complexity |

### Segmentation Matrix Format

Create a 2D matrix with candidate segments plotted. Each cell = a distinct market opportunity.

```
            [Dimension 2 →]
            Col A    Col B    Col C
[D1] Row 1  Seg 1    Seg 2    Seg 3
     Row 2  Seg 4    Seg 5    Seg 6
     Row 3  Seg 7    Seg 8    Seg 9
```

Then identify which segments are primary targets for Phase 2 analysis.

### Killer Application Priority List

Rank the top 5 use-cases / applications in priority order:

| Priority | Application | Rationale |
|---------|------------|-----------|
| #1 | [application] | [why this is the strongest differentiator / wedge] |
| #2 | | |
| #3 | | |
| #4 | | |
| #5 | | |

---

## Tool 2: SPAN Analysis (Strategic Position Analysis)

**Purpose**: Prioritise market segments / product offerings by plotting Market Attractiveness vs Competitive Position. Used to allocate investment across segments.

### SPAN Axes — FIXED DEFINITIONS

**Y-Axis: Market Attractiveness** (sub-factors):
1. Market opportunity size (relative SAM)
2. Market growth rate
3. Profitability potential (sub-factors: direct/indirect competition, new entrant threat, buyer/supplier pressure)
4. Strategic value (importance of entering this market)

**X-Axis: Competitive Position** (sub-factors):
1. Current market share (or realistic achievable share)
2. Differentiated product characteristics
3. Development/manufacturing cost vs competitors
4. SG&A cost efficiency vs competitors
5. Core competencies match

**Bubble Size**: Proportional to 3-year SAM (total addressable market for that segment)

### SPAN Scoring Table Format

| Factor | Weight | Market A | Market B | Market C | Market D |
|--------|--------|---------|---------|---------|---------|
| **Y: Market Attractiveness** | | | | | |
| Market size (relative) | | | | | |
| Growth rate | | | | | |
| Profitability potential | | | | | |
| Strategic value | | | | | |
| **Y-axis weighted score** | | | | | |
| **X: Competitive Position** | | | | | |
| Regulatory leverage | | | | | |
| Entry barrier (our side) | | | | | |
| Differentiation deliverable | | | | | |
| Core competency match | | | | | |
| **X-axis weighted score** | | | | | |
| **SPAN Recommendation** | | | | | |

### SPAN Matrix Visual

Represent as a 2D matrix in the output:
```
Y: Market Attractiveness
HIGH │  ●Mkt_C        ●Mkt_B
     │
     │       ●Mkt_D        ●Mkt_A
     │
LOW  └──────────────────────────────
    LOW    X: Competitive Position    HIGH

● Bubble size ≈ 3-year SAM
```

### SPAN Investment Recommendations

Based on SPAN position:
- **High Y + High X** → Invest / Go (primary)
- **High Y + Low X** → Redirect / Selective Go (fix X first or find niche)
- **Low Y + High X** → Maintain / Low investment
- **Low Y + Low X** → Divert / Avoid

---

## Tool 3: FAN — Financial Analysis

**Purpose**: Validate SPAN recommendations with financial modelling. Converts market opportunity into revenue projections.

### FAN Structure (per market / segment)

Work through this chain for each target market:

```
Total Market Size (TAM)
    ↓ × Addressable Rate
SAM (Serviceable Addressable Market)
    ↓ × Target Market Share (%)
Target Revenue (Gross)
    ↓ × Gross Margin Rate
Gross Margin ($)
    ↓ - SG&A (% of Revenue)
    ↓ - R&D/E (% of Revenue)
Operating Profit
```

### FAN Summary Table Format

| Metric | Market A | Market B | Market C | Market D |
|--------|---------|---------|---------|---------|
| Market CAGR | | | | |
| 3yr SAM estimate | | | | |
| Target units / installations | | | | |
| ASP (hardware) | | | | |
| 3yr Hardware Revenue | | | | |
| Software / Service attach rate | | | | |
| **3yr Total Revenue (est.)** | | | | |
| Key cost items | | | | |
| **Financial Viability** | ✓ / △ / ✗ | | | |

### FAN Assumptions to Document

Always state the key assumptions:
- ASP basis (list price? expected selling price with distributor margin?)
- Market share ramp assumption (Year 1 / Year 2 / Year 3)
- Distributor margin % applied
- Service contract attach rate
- FX assumptions if multi-currency

---

## Tool 4: Business Concept Design

**Purpose**: Define the business model for the target market. IBM's Business Concept Design Table captures the full commercial logic.

| Item (IBM) | Description / Question | Answer |
|-----------|----------------------|--------|
| **Customer** | Who is the customer? Who is the end user? Target segment? | |
| **Value Proposition** | What unique value do we offer? Why do customers buy from us vs competitors? What delights them? | |
| **Value Capture** | Profit model? Who pays? How do we price? Revenue sources? | |
| **Scope of Activities** | What do we do? What do we not do? Make vs buy decisions? | |
| **Strategic Control** | What prevents competitors from copying us? What creates lock-in or defensibility? | |
| **Key Success Factors** | What must be true for this to work? | |

**Output note**: The Value Proposition should be expressible as a single sentence positioning statement. Test: Can a distributor or KOL repeat it accurately?

---

## Phase 2 → Phase 3 Transition

Before moving to Phase 3, confirm:
- [ ] Segmentation dimensions defined (not country-only)
- [ ] Killer applications ranked
- [ ] SPAN completed with correct Y/X axes and bubble sizes
- [ ] FAN validates top SPAN recommendations financially
- [ ] Business Concept Design table complete

**DCP2 checkpoint**: Senior management confirms which markets to enter (Go / Redirect / Defer) based on SPAN + FAN before Phase 3 execution planning begins.
