---
name: ibm-market-planning
description: |
  Apply the IBM Market Planning (MP) Methodology to produce structured market entry and go-to-market strategies. Use this skill whenever the user wants to:
  - Analyse a new product or market for international expansion
  - Build a go-to-market or market entry strategy
  - Evaluate an existing strategy against the IBM MP framework
  - Produce structured outputs (markdown, PPTX, Excel) from the IBM framework
  - Prioritise markets using SPAN / FAN methods
  - Design channel / coverage plans or ABP execution milestones

  Trigger on: "market entry strategy", "go-to-market", "IBM framework", "SPAN analysis", "market planning", "growth strategy", "international expansion", "GTM", "STEEP analysis", "6 forces", "Cross SWOT", "value net", "incubation milestone", "coverage plan", "DCP decision", "growth gap", or any request for a structured market strategy.

  ALWAYS use this skill before producing any IBM-style market analysis output, even if the user hasn't named the IBM framework explicitly.
---

# IBM Market Planning (MP) Skill

Applies IBM's end-to-end Market Planning Methodology to produce rigorous, structured market strategy outputs.

---

## Skill Overview

IBM MP is a three-phase framework used to move from market opportunity to executable plan:

```
Phase 1 — WHY       Phase 2 — WHAT        Phase 3 — HOW
"決定投入市場"        "決定進攻策略"           "執行進入市場"
─────────────────   ──────────────────    ──────────────────────
Goal & Growth Gap   Market Segmentation   Solution Roadmap
4C Definition    →  SPAN Analysis      →  Value Net (物/金/資訊流)
STEEP (Macro)       FAN Financial         Coverage Plan
6 Forces (Micro)    Business Concept      ABP + Incubation Miles.
Competitor Gap      Design                DCP Decision Gates
Value Chain
Cross SWOT
```

**DCP (Decision Check Points)** gate transitions between phases: DCP1 = invest or not, DCP2 = which strategy, DCP3 = execution calibration.

---

## How to Use This Skill

### Step 1 — Clarify Inputs

Before starting, confirm:

1. **Product / Service**: What is being taken to market?
2. **Current situation**: What regulatory assets exist (FDA, CE, local)? What clinical/commercial evidence exists?
3. **Known constraints**: Legal risks, timeline, resource limits, markets already ruled out
4. **Existing analyses**: Has any prior strategy/analysis been done? (If yes → run Assessment Mode first)
5. **Desired output**: Full strategy doc? PPTX? Country prioritisation only? Specific phase only?

### Step 2 — Choose Mode

| Mode | When to Use | Go to |
|------|------------|-------|
| **Full IBM Analysis** | New product or market, no prior strategy | Run all three phases in sequence |
| **Assessment Mode** | Existing analysis (e.g. from GPT/consultant) — evaluate vs IBM | See Assessment Mode section below |
| **Phase-Only** | User needs only one phase (e.g. just SPAN, just Coverage Plan) | Jump to that phase reference |
| **Output-Only** | Analysis complete, need PPTX/Excel/doc | See Output Formats section |

---

## PHASE 1 — WHY: Growth Market Strategy

**Read `references/phase1-why.md` for full tool instructions.**

Phase 1 establishes WHY a market is worth entering. Outputs:
- Defined growth targets (BAU + Incremental GI breakdown)
- 4C player map (Customer / Company / Competitor / Collaborator)
- STEEP macro environment table
- 6 Forces industry structure
- Competitor gap matrix
- Value chain positioning
- Cross SWOT → Strategic Areas with Top 3 Actions per quadrant

**Phase 1 output format**: Structured tables + narrative. Each tool produces a self-contained table that feeds the next.

---

## PHASE 2 — WHAT: Segmentation Strategy

**Read `references/phase2-what.md` for full tool instructions.**

Phase 2 decides WHERE to attack and WITH WHAT. Outputs:
- Market segmentation (avoid single-dimension country-only; use Clinical Application × Market Role or equivalent)
- Killer Application priority list
- SPAN matrix (Y = Market Attractiveness; X = Competitive Position; Bubble = 3yr SAM)
- FAN financial analysis per segment (SAM → Share → Revenue → Margin)
- Business Concept Design table (Customer / Value Proposition / Value Capture / Scope / Strategic Control / KSF)

**Phase 2 output format**: SPAN produces a 2D matrix visual + scoring table. FAN produces a per-market financial table.

---

## PHASE 3 — HOW: Business Execution Plan

**Read `references/phase3-how.md` for full tool instructions.**

Phase 3 defines HOW to execute. Outputs:
- Product Architecture / Solution Roadmap (NOW / Year 1-2 / Year 2-3)
- Value Net: 物流 (Product Flow) / 金流 (Financial Flow) / 資訊流 (Information Flow)
- Coverage Plan: Direct vs Indirect, by market
- ABP: 30 / 60 / 90 Day Critical Tasks + Incubation Milestones (go/no-go gates per market)
- DCP Decision Position Sheet (Go / Redirect / Defer per market/initiative)

---

## Assessment Mode — Evaluate Existing Analysis vs IBM

When the user provides an existing strategy document (from GPT, consultant, internal):

1. Map each section of the existing analysis to IBM phases/tools
2. Score completeness: ✓ Done / △ Partial / ✗ Missing
3. For each ✗ or △ item: identify the gap and produce the missing output
4. Produce a summary table: "GPT/Existing Analysis vs IBM Framework — Gap Assessment"

**Standard gap table format:**

| IBM Tool | Existing Score | Gap / Issue | Action |
|----------|---------------|-------------|--------|
| Growth Gap (BAU vs Incremental) | ✗ Missing | Jumped directly to conclusions without BAU/GI split | Produce Growth Gap waterfall |
| SPAN (proper Y/X axes) | △ Partial | Used custom weighted score; not IBM SPAN structure | Rebuild SPAN with correct axes |
| FAN (per-market financials) | ✗ Missing | Revenue targets not grounded in SAM/share logic | Build FAN table |
| Value Net | ✗ Missing | Covered Coverage Plan only | Add 物流/金流/資訊流 |
| ... | ... | ... | ... |

---

## Output Formats

### Markdown Strategy Doc
- Use `##` for each IBM tool (Goal & Growth Gap, 4C, STEEP…)
- Tables for all structured data (no prose lists for analytical content)
- Bilingual headers where needed (e.g. "Value Net — 物流 / 金流 / 資訊流")
- Executive summary at top; DCP summary at end

### PPTX Presentation
**Read the `pptx` skill (`/mnt/skills/public/pptx/SKILL.md`) before generating slides.**

Standard slide structure (21 slides):
1. Cover
2. IBM Framework Overview (WHY/WHAT/HOW)
3. Assessment (if applicable)
4. Section: WHY
5. Goal & Growth Gap (BAU waterfall + gap table)
6. 4C Player Definition (2×2 quadrant cards)
7. STEEP Analysis (table with Macro | 機會 | 威脅)
8. 6 Forces + Competitor Gap
9. Cross SWOT (2×2 matrix)
10. Section: WHAT
11. Market Segmentation + Killer Apps
12. SPAN Analysis (bubble matrix + scoring table)
13. FAN Financial Analysis (per-market table)
14. Business Concept Design
15. Section: HOW
16. Solution Roadmap (timeline table)
17. Value Net (3-column: 物流/金流/資訊流)
18. Coverage Plan (by market)
19. ABP + Incubation Milestones (30/60/90 + milestone table)
20. DCP Decision Sheet
21. Strategy Summary + Evidence Flywheel

**Colour palette**: Use navy (#0F2A44) as dominant, teal (#0B7A8F) secondary, mint (#00B4A6) accent. Dark background for cover, section dividers, summary. Light (#F0F7FA) for content slides.

### Excel Tracker
Produce an `.xlsx` with sheets:
- **Market Priority**: SPAN scoring table + DCP decision per market
- **FAN**: Per-market financial model (SAM → Share → Revenue → Margin → SG&A)
- **ABP**: 30/60/90 action tracker with Owner / Status / Due Date
- **Incubation Milestones**: Milestone × Market matrix with go/no-go status
- **Coverage Plan**: Partner type, model, KPI per market

---

## Key Principles (from IBM MP Methodology)

1. **Growth Gap first**: Always separate BAU growth from Incremental GIs before recommending markets. Never jump to country prioritisation without establishing the financial waterfall.

2. **SPAN axes are fixed**: Y-axis = Market Attractiveness (market size, growth rate, profitability/competition/entry threat, strategic value). X-axis = Competitive Position (market share, differentiation, cost structure, core competencies). Bubble size = 3-year SAM. Do not substitute custom weighted scores.

3. **FAN validates SPAN**: Every SPAN recommendation must be grounded in FAN (SAM → Market Share Assumption → Revenue → Margin → SG&A → R&D).

4. **Value Net is mandatory in Phase 3**: Physical Flow / Financial Flow / Information Flow must each be explicitly designed. Coverage Plan alone is not sufficient for the HOW phase.

5. **Incubation Milestones ≠ 30/60/90**: IBM requires per-market go/no-go milestones (Year 1 / Year 2 / Year 3) as DCP decision inputs. 30/60/90 is the near-term action plan, not the incubation gate.

6. **Cross SWOT → Top 3 Actions per quadrant**: Each of the 4 Cross SWOT quadrants (Business Opportunity / Market Creation / Transformation / Business Risk) must produce Top 3 concrete actions, not just strategic statements.

7. **Segmentation ≠ country list**: IBM segmentation requires at least two dimensions. For medical/tech products: Clinical Application × Market Entry Role. Avoid defaulting to "list of target countries" as the sole segmentation output.

---

## Reference Files

| File | Read When |
|------|-----------|
| `references/phase1-why.md` | Running Phase 1 tools (Goal, 4C, STEEP, 6 Forces, Competitor, Value Chain, Cross SWOT) |
| `references/phase2-what.md` | Running Phase 2 tools (Segmentation, SPAN, FAN, Business Concept Design) |
| `references/phase3-how.md` | Running Phase 3 tools (Roadmap, Value Net, Coverage Plan, ABP, DCP) |

---

## Quick Reference: Common Failure Modes to Flag

When reviewing any market strategy output (from user, GPT, consultant), immediately flag:

- ❌ Revenue targets with no SAM/market share grounding → needs FAN
- ❌ Country priority list with no SPAN axes → rebuild SPAN
- ❌ "We will use distributors" without 物流/金流/資訊流 design → needs Value Net
- ❌ "30/60/90 action plan" as the only HOW output → add Incubation Milestones
- ❌ SWOT table without Cross SWOT strategic areas → extend to Cross SWOT
- ❌ Product features listed without Value Chain positioning → add Value Chain
- ❌ Market entry strategy missing DCP position sheet → add DCP
