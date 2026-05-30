# ibm-market-planning

A Claude Code skill that applies the **IBM Market Planning (MP) Methodology** to produce rigorous, structured market entry and go-to-market strategies.

## What It Does

Guides you through IBM's three-phase market planning framework — from strategic intent to executable plan — and produces structured outputs (Markdown, PPTX, Excel).

```
Phase 1 — WHY          Phase 2 — WHAT         Phase 3 — HOW
"決定投入市場"           "決定進攻策略"            "執行進入市場"
──────────────────     ────────────────────    ──────────────────────
Goal & Growth Gap      Market Segmentation     Solution Roadmap
4C Definition       →  SPAN Analysis        →  Value Net (物/金/資訊流)
STEEP (Macro)          FAN Financial           Coverage Plan
6 Forces (Micro)       Business Concept        ABP + Incubation Miles.
Competitor Gap         Design                  DCP Decision Gates
Value Chain
Cross SWOT
```

**DCP (Decision Check Points)** gate transitions between phases:
- DCP1 = invest or not
- DCP2 = which strategy
- DCP3 = execution calibration

## Installation

### Via Claude Code CLI
```bash
# Download the .skill file from Releases and run:
claude skill install ibm-market-planning.skill
```

### Manual
```bash
# Unzip into your Claude skills directory
unzip ibm-market-planning.skill -d ~/.claude/skills/
```

## Usage

Invoke the skill in Claude Code:

```
/ibm-market-planning
```

Or describe what you need — the skill auto-triggers on keywords like:

> "market entry strategy", "go-to-market", "SPAN analysis", "international expansion", "GTM", "STEEP analysis", "6 forces", "Cross SWOT", "value net", "coverage plan", "DCP decision", "growth gap"

## Modes

| Mode | When to Use |
|------|------------|
| **Full IBM Analysis** | New product/market, no prior strategy — runs all three phases |
| **Assessment Mode** | Existing strategy from GPT/consultant — gaps vs IBM framework |
| **Phase-Only** | Need only one phase (e.g. just SPAN, just Coverage Plan) |
| **Output-Only** | Analysis done, need PPTX / Excel / Markdown doc |

## Output Formats

- **Markdown** — Structured strategy document with IBM-standard tables
- **PPTX** — 21-slide deck (navy/teal palette, bilingual headers)
- **Excel** — Market Priority / FAN / ABP / Incubation Milestones / Coverage Plan sheets

## Key Principles Enforced

1. **Growth Gap first** — Always separate BAU from Incremental GIs before recommending markets
2. **SPAN axes are fixed** — Y = Market Attractiveness, X = Competitive Position, Bubble = 3yr SAM
3. **FAN validates SPAN** — Every SPAN recommendation grounded in SAM → Share → Revenue → Margin
4. **Value Net is mandatory** — Physical / Financial / Information Flow, not just Coverage Plan
5. **Incubation Milestones ≠ 30/60/90** — Per-market Year 1/2/3 go/no-go gates required
6. **Cross SWOT → Top 3 Actions** — Each quadrant produces concrete actions, not just statements
7. **Segmentation ≠ country list** — Requires at least two dimensions (e.g. Application × Market Role)

## File Structure

```
ibm-market-planning/
├── SKILL.md                    # Main skill definition and instructions
├── README.md                   # This file
└── references/
    ├── phase1-why.md           # Phase 1 tool instructions (Goal, 4C, STEEP, 6 Forces, Competitor, Value Chain, Cross SWOT)
    ├── phase2-what.md          # Phase 2 tool instructions (Segmentation, SPAN, FAN, Business Concept)
    └── phase3-how.md           # Phase 3 tool instructions (Roadmap, Value Net, Coverage Plan, ABP, DCP)
```

## Real-World Example

This skill was used to produce a full IBM Market Planning strategy for **SURGIMAGE SIM 1000H** — a fluorescence-guided surgery imaging platform — covering:

- 5-market international expansion (Australia, UK, Singapore, Japan, US)
- SPAN prioritisation with FAN financial validation
- On-demand VPN + Exchange → Notion automated pipeline integration
- Full 41-slide PPTX output

## Common Failure Modes It Catches

- ❌ Revenue targets with no SAM/market share grounding → builds FAN
- ❌ Country priority list with no SPAN axes → rebuilds SPAN correctly
- ❌ "We will use distributors" without 物流/金流/資訊流 → adds Value Net
- ❌ "30/60/90 plan" as the only HOW output → adds Incubation Milestones
- ❌ SWOT without Cross SWOT strategic areas → extends to Cross SWOT
- ❌ Market entry strategy missing DCP sheet → adds DCP

## License

MIT
