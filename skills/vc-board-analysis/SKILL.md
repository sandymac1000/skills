---
name: vc-board-analysis
description: "Structured board material review for a VC partner with a software, ML, and AI portfolio approaching exit. Produces a 5-section investment analysis (Situation, Financial Trajectory, Commercial Momentum, Product & AI/ML Position, Exit Readiness) capped at 800 words. Trigger when the user shares board materials, board packs, investor updates, quarterly reports, management accounts, or asks for board prep, pre-meeting review, or portfolio company analysis. Also trigger for lightweight financial snapshot mode when only management accounts or financial data are provided. Optimised for mature software/ML/AI companies at Series B–D approaching exit horizon. Current portfolio: Lifebit, Stacker/Outportal, nPlan, EOLA."
---

# VC Board Material Analysis

A focused analysis instrument for a small, known portfolio of mature software and AI/ML companies approaching exit. Produces either a full 5-section board review (capped at 800 words) or a lightweight financial snapshot, depending on input. Written for a VC partner and co-investors. Emphasis throughout on trajectory vs. plan and exit readiness.

## When to use this skill

Trigger when the user:
- Uploads or shares a board deck, board pack, investor update, or quarterly report (PDF or PPT)
- Shares management accounts, financial statements, or financial data only
- Asks for "board prep", "pre-board review", "board analysis", or "portfolio company review"
- Needs to synthesise materials before a partner meeting, IC discussion, or LP update
- Wants a structured read of any Lifebit, Stacker, nPlan, or EOLA report or update

## How to use this skill

### Step 1: Identify input type and select mode

**Full board pack mode** — use when input is a complete board deck, board pack, or investor update (PDF, PPT, or pasted content). Produce the full 5-section analysis.

**Financial snapshot mode** — use when input is management accounts, financial statements, or financial data only, without a full board pack. Produce the lightweight financial extraction template instead.

If the company is known (Lifebit, Stacker/Outportal, nPlan, EOLA), apply company-specific context from the company context section before producing either output.

If materials are incomplete, ask **one** targeted clarifying question — prioritise the gap most likely to change the exit assessment. Do not ask multiple questions upfront.

### Step 2A: Full board pack — apply the five-section framework

Produce the analysis using the template below. Adhere strictly to per-section word budgets. **Total output must not exceed 800 words. This is a hard cap — not a guideline.**

---

## Full Board Pack Output Template

```
BOARD ANALYSIS — [Company Name] | [Meeting Date or Quarter]
Stage: [Series A / B / C / Growth]
Model: [SaaS / Platform / Marketplace / API / Other]
RAG: [RED / AMBER / GREEN] — [one-line rationale]
Exit Horizon: [<12m / 12–24m / 24–36m / 36m+]
```

---

### 1. Situation (~120 words)

- **Headline**: One sentence on what this board meeting is fundamentally about — e.g. bridge decision, commercial inflection, M&A process initiation, plan reset.
- **RAG status**: Own this judgment call directly. RED = at-risk (capital, team, or thesis); AMBER = tracking but flagged; GREEN = on-plan or ahead.
- **Trajectory signal**: Is the company accelerating, flat, or decelerating vs. the plan set at last raise? State the direction explicitly.
- **Board asks**: Bullet the explicit requests the company is making of the board. If asks are absent or vague, flag it — that is itself a signal about management maturity.

---

### 2. Financial Trajectory (~175 words)

- **Runway**: Months of cash at current burn. Note any extension scenarios.
- **Burn vs. growth**: Is burn increasing proportionally with growth, or diverging? Flag burn acceleration without corresponding ARR progress.
- **Revenue**: ARR or MRR vs. plan — state the number, the delta vs. last period, and the direction. "Revenue is growing" is not acceptable. "ARR grew 18% QoQ to £3.2M, 12% behind plan" is.
- **Unit economics**: NRR, gross margin, CAC/LTV where disclosed. Note trend direction.
- **Next raise**: Timeline, target size, syndicate signals. Assess readiness vs. ambition honestly.
- **Red flags**: Unreconciled actuals vs. budget, deferred payables, missing financial tables, or signs of financial engineering in the pack.

---

### 3. Commercial Momentum (~175 words)

- **Pipeline**: Stage-weighted pipeline value or leading indicator. Note velocity change vs. prior quarter.
- **Wins and losses**: Named customer or partnership developments. Note enterprise deals, strategic partnerships, or significant churn events.
- **Expansion revenue**: NRR and land-and-expand evidence. For AI/ML platforms — are customers expanding usage as the model improves, or is adoption plateauing?
- **Pricing power**: Any changes to pricing, contract structure, or revenue model. Flat or declining ASP in an AI product is a competitive signal.
- **Competitive position**: New entrants, pricing pressure, or platform displacement risk. Note if foundation model commoditisation is affecting differentiation narrative.

---

### 4. Product & AI/ML Position (~175 words)

- **Milestones**: What was delivered vs. committed at the last board meeting. Be explicit about slippage and its cause.
- **AI/ML lens**:
  - *Data moat*: Is proprietary training data or feedback loops compounding over time? Is the moat widening or being eroded?
  - *Model provenance*: Proprietary, fine-tuned, or wrapper-layer only? Wrapper-layer products face acute commoditisation risk.
  - *Generative approach maturity*: For Stacker/Outportal and nPlan — is generative capability differentiated or replicable? Evidence of customer lock-in through generated artefacts or workflows?
  - *Federation architecture*: For Lifebit — is federated compute genuinely defensible or a replicable deployment pattern?
  - *Inference economics*: Are AI serving costs declining as % of revenue, or a margin headwind at scale?
- **IP and patent position**: For Lifebit and nPlan — patents granted or pending, freedom-to-operate status, and whether the patent portfolio strengthens the M&A value case or is purely defensive. Flag any gaps in IP documentation.
- **Roadmap realism**: Next-quarter deliverables vs. team size and capital available.

---

### 5. Exit Readiness (~155 words)

- **Horizon**: Best estimate — <12m / 12–24m / 24–36m / 36m+. State the basis.
- **Exit route**: IPO, strategic acquisition, secondary, or PE buyout — rank the credible options given current scale and market conditions.
- **Strategic acquirer mapping**:
  - *Lifebit*: Health data platform buyers — pharma informatics, cloud hyperscalers with health verticals, genomics infrastructure consolidators. Patent portfolio is a specific value driver for acquirers seeking defensible federated architecture IP.
  - *nPlan*: Construction tech strategics, infrastructure software consolidators, risk/insurance platforms. Historical project data moat and any granted patents are key value signals for strategic buyers.
  - *Stacker/Outportal*: Enterprise GenAI platform buyers, no-code/low-code consolidators, vertical SaaS acquirers.
  - *EOLA*: Vertical marketplace consolidators, outdoor/leisure PE, booking platform roll-ups.
- **Thesis integrity**: Does this board pack confirm, challenge, or weaken the original investment thesis? State plainly.
- **Value creation levers**: Top two actions the board can take before exit to protect or increase exit value.

---

## Step 2B: Financial snapshot mode

Use when only management accounts or financial data are provided. Produce this lightweight extraction:

```
FINANCIAL SNAPSHOT — [Company Name] | [Period]

Revenue
  ARR / MRR:        £Xm  (vs £Xm prior period — +/-X%)
  vs Plan:          X% ahead / behind
  Trend:            Accelerating / Flat / Decelerating

Burn & Runway
  Monthly burn:     £Xk  (vs £Xk prior — +/-X%)
  Runway:           X months at current burn
  Extension levers: [bridge / cost reduction / revenue acceleration / none stated]

Unit Economics
  Gross margin:     X%  (vs X% prior)
  NRR:              X%
  CAC / LTV:        [if disclosed]

Exit Relevance
  [2–3 sentences: what do these numbers mean for exit timing and valuation?
   Are they moving toward or away from exit-readiness thresholds?
   Any specific metrics that a strategic acquirer or PE buyer would flag?]

Data Quality
  [Note any missing, inconsistent, or unreconciled figures as DATA ABSENT]
```

---

## Output discipline

- **Hard cap: 800 words** for full board pack mode. Financial snapshot has no cap but must be concise.
- Write in third person, present or past tense as appropriate.
- Cut filler: no "it is worth noting", "importantly", "the company continues to", "encouragingly".
- Use precise language with numbers: "ARR grew 23% QoQ to £2.1M, 8% behind plan" not "revenue is growing well".
- Flag missing information as `[DATA ABSENT]` — never infer or omit silently.
- RAG status and Exit Horizon are judgment calls — state them, own them, justify in one line each.
- Trajectory direction (accelerating / flat / decelerating) must be stated explicitly in sections 1, 2, and 3.

## Input handling

- **PDF**: Read natively — preferred format for board decks.
- **PPT / PPTX**: Read natively — if formatting is ambiguous, note it and work with available content.
- **Pasted text**: Accepted in any format.
- **Management accounts (Excel/CSV)**: Extract figures directly into financial snapshot mode.

## Company context

**Lifebit** — Federated genomics and health data platform. Privacy-preserving federated compute enabling cross-institutional data analysis without data movement. Data moat via institutional partnerships. Patent portfolio around federated architecture — a specific M&A value driver. Watch: hyperscaler competition, federation replicability, enterprise contract expansion.

**Stacker / Outportal** — Generative application and content platform. GenAI-native workflow generation. Watch: foundation model commoditisation risk, proprietary data layer defensibility, enterprise vs. SMB mix shift.

**nPlan** — AI-driven construction project risk prediction and scenario planning. Historical project data moat and generative scenario modelling. Patent position around AI-driven project risk methodology. Watch: data moat depth vs. new entrants, enterprise sales cycle length, third-party integration dependencies.

**EOLA** — Outdoor activity booking and management platform. Vertical marketplace with operator tooling. Watch: take rate sustainability, geographic expansion execution, competitive consolidation in leisure booking.

## Keywords

board pack, board meeting, board prep, investor update, portfolio review, VC analysis, quarterly review, board materials, pre-board, investment analysis, portfolio company, IC prep, exit readiness, AI/ML, Lifebit, Stacker, nPlan, EOLA, software portfolio, exit horizon, strategic acquirer, management accounts, financial snapshot, patents, IP moat
