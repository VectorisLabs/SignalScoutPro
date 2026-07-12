# SignalScout Business Impact and Decision Simulation

**Status:** Product baseline  
**Effective date:** 2026-07-12  
**Scope:** Product strategy, round-two demo, UX, business-impact reasoning, POC evolution, and production requirements  
**Audience:** Product, design, engineering, mentors, judges, and future implementation agents

## 1. Purpose

SignalScout must go beyond detecting corporate warning signals. It must help a business decision-maker understand:

1. why the evidence matters;
2. which reasoning framework was applied;
3. which strategic choices are available;
4. what consequences may follow from each choice;
5. how much financial value may be exposed by acting too late or overreacting too early.

The product outcome is not a risk score. The product outcome is a more informed, evidence-backed business decision.

## 2. Round-Two Mentor Feedback

The round-two direction was informed by the following mentor guidance:

- make the interface friendlier;
- make advice explanations visually clear and persuasive;
- show source links prominently;
- expose the reasoning process and theoretical framework;
- forecast the consequences of a decision;
- simulate the results of strategic choices;
- emphasize business results and business impact;
- show that a wrong business decision may cost millions or billions of dollars.

This feedback changes the presentation priority, not the evidence-first foundation of SignalScout.

## 3. Product Positioning

### 3.1 Short definition

SignalScout is an evidence-backed strategic decision simulator for counterparty and corporate-change risk.

### 3.2 Value proposition

SignalScout converts scattered corporate warning signals into explainable strategic scenarios. It helps executives compare the financial and operational consequences of maintaining, adapting, or accelerating their response.

### 3.3 Core business claim

SignalScout makes the cost of a wrong business decision visible before the decision is made.

### 3.4 What SignalScout must not claim

SignalScout must not claim that it can predict bankruptcy or certify a future outcome. It provides scenario-based decision support using verified evidence, explicit assumptions, bounded calculations, and visible limitations.

Prefer these terms:

- scenario projection;
- consequence simulation;
- exposure forecast;
- decision-impact range;
- evidence-backed decision support.

Avoid these terms unless independently validated:

- guaranteed outcome;
- exact future loss;
- bankruptcy prediction;
- certain financial impact;
- autonomous business decision.

## 4. Decision Reasoning Framework

The user must be able to inspect the complete reasoning chain:

```text
Verified evidence
  -> Signal
  -> Pattern
  -> Business driver
  -> Financial and operational exposure
  -> Strategic choices
  -> Consequence simulation
  -> Recommended decision posture
```

### 4.1 Evidence

Show the verified source, publication time, exact supporting excerpt, stable evidence ID, and a clear source link.

### 4.2 Signal

Normalize the event into a business-relevant signal such as workforce reduction, delayed filing, covenant event, executive departure, capital-expenditure reduction, or operating-footprint reduction.

### 4.3 Pattern

Explain how independent signals form a larger pattern. Repeated reporting of the same underlying event must not inflate maturity or risk.

### 4.4 Business driver

Translate the pattern into a decision-relevant mechanism, for example:

- increasing liquidity pressure;
- reduced operating capacity;
- deteriorating payment reliability;
- demand contraction;
- supplier concentration risk;
- higher disruption or replacement cost.

### 4.5 Exposure

Connect the business driver to the user's actual financial and operational exposure. Do not infer private exposure values from public evidence.

### 4.6 Strategic choices

The primary decision postures are:

- `MAINTAIN`: preserve the current relationship and operating terms;
- `ADAPT`: reduce or reshape exposure while retaining part of the opportunity;
- `ACCELERATE`: act quickly to maximize protection or strategic repositioning.

### 4.7 Consequences

For each posture, show potential downside protection, revenue retained, capital at risk, opportunity cost, transition cost, and operational disruption.

### 4.8 Recommendation

The recommendation must state:

- why the posture fits the current evidence;
- why the other postures are not preferred;
- which assumptions materially affect the result;
- what evidence could disprove the recommendation;
- which trigger should cause a reassessment.

## 5. Financial Impact Framework

Financial impact must be calculated from user-provided values, approved internal data, or clearly labelled illustrative demo inputs.

### 5.1 Commercial exposure

```text
Total commercial exposure
= accounts receivable
+ inventory in transit
+ non-cancellable commitments
+ replacement or switching cost
```

### 5.2 Scenario-adjusted loss exposure

```text
Scenario-adjusted loss exposure
= total commercial exposure
x loss-severity range
```

The loss-severity range must be an explicit assumption or originate from an approved model. SignalScout must not silently invent a probability or severity value.

### 5.3 Cost of overreaction

```text
Cost of overreaction
= lost contribution margin
+ transition cost
+ relationship and opportunity cost
```

### 5.4 Decision value

```text
Decision value
= avoided downside
- mitigation cost
- opportunity cost
```

### 5.5 Required presentation rules

- Show ranges rather than false precision when uncertainty is material.
- Show the currency, period, unit, and source of every input.
- Separate observed facts from user assumptions and calculated outputs.
- Label illustrative values prominently.
- Never use a large dollar figure only for presentation impact.
- Show sensitivity when one assumption materially changes the recommendation.

## 6. UX Requirements

### 6.1 Executive Decision Header

The first screen should lead with the decision, not the technology or a raw risk score.

```text
Decision: How should we manage exposure to this counterparty?
Current posture: ADAPT
Financial exposure under review: [range]
Decision window: [time horizon]
Confidence: [level with explanation]
```

### 6.2 Why This Matters

Provide a short explanation of:

- what changed;
- why it affects the user's business;
- which exposure is involved;
- how urgent the decision is.

Include direct actions for `Why we think this`, `View evidence`, and `What could disprove it`.

### 6.3 Evidence Cards

Each evidence card should contain:

- stable evidence ID;
- source title and source type;
- public availability date;
- exact approved excerpt;
- a clear external source link;
- approval or limitation status.

Pending or rejected candidates must remain visually and semantically separate from approved evidence.

### 6.4 Reasoning Explorer

Render the reasoning framework as inspectable steps rather than one opaque paragraph. Users should be able to move from a recommendation back to its business driver, pattern, signals, and evidence.

### 6.5 Strategic Scenario Simulator

Compare `MAINTAIN`, `ADAPT`, and `ACCELERATE` using the same dimensions:

| Dimension | MAINTAIN | ADAPT | ACCELERATE |
|---|---|---|---|
| Typical action | Preserve current terms | Reduce or reshape exposure | Maximize protection or reposition quickly |
| Revenue retained | Highest initially | Moderate to high | Lowest initially |
| Capital at risk | Highest | Reduced | Lowest |
| Disruption cost | Lowest | Moderate | Highest |
| Downside if warning is correct | Highest | Controlled | Lowest |
| Downside if warning is wrong | Lowest | Moderate | Highest |

The simulator should accept bounded inputs such as:

- accounts receivable;
- monthly sales;
- committed purchase orders;
- inventory in transit;
- gross margin;
- loss-severity range;
- switching cost;
- decision horizon.

### 6.6 Consequence View

For every posture, show:

- potential exposed capital;
- potential downside avoided;
- revenue retained or placed at risk;
- mitigation and transition cost;
- operational disruption;
- assumptions and sensitivity;
- evidence coverage and confidence.

### 6.7 Recommendation Explanation

Use a structured explanation:

```text
Recommended posture: ADAPT

Why:
- [supported reason]
- [supported reason]

Why not MAINTAIN:
- [trade-off or risk]

Why not ACCELERATE:
- [trade-off or insufficient evidence]

Re-evaluate when:
- [observable trigger]
- [observable trigger]
```

Color must not be the only carrier of meaning. Links, assumptions, evidence state, and blockers must be keyboard accessible and understandable to non-technical executives.

## 7. POC and Production Boundaries

### 7.1 Round-Two POC

The POC should prove the decision experience using a frozen, cited case and deterministic calculations:

- one deeply researched historical case;
- user-adjustable or explicitly illustrative exposure inputs;
- `MAINTAIN`, `ADAPT`, and `ACCELERATE` comparison;
- transparent formulas and assumptions;
- evidence-linked explanations;
- consequence ranges;
- visible limitations and reassessment triggers;
- reliable offline operation for judging.

The POC does not need to prove market-wide forecasting, live enterprise data integration, or autonomous execution of strategic actions.

### 7.2 Target Production Form

Production may add:

- authenticated organization-specific exposure data;
- persistent scenario and assumption versions;
- role-based access and approval workflows;
- deterministic simulation services;
- portfolio and multi-company monitoring;
- scheduled evidence collection;
- event-driven recalculation;
- model and rule version audit trails;
- sensitivity analysis and calibrated domain models;
- integration with ERP, procurement, CRM, and risk systems.

Production architecture documents should describe how these capabilities are implemented. This document remains the product and business baseline they must satisfy.

## 8. Round-Two Presentation Narrative

The presentation should prioritize:

1. the expensive business decision;
2. the evidence and reasoning framework;
3. the strategic alternatives;
4. the consequence and exposure simulation;
5. explainability and trust;
6. the target production architecture.

Recommended pitch:

> Most risk tools stop at telling you that something looks dangerous. SignalScout goes one step further. It shows executives why the risk matters, what strategic choices they have, and the financial consequence of each choice. A wrong supplier or counterparty decision can expose millions or billions in receivables, inventory, commitments, and lost revenue. SignalScout turns verified evidence into an explainable decision before that value is lost.

Any statement about millions or billions must be presented as addressable exposure or a scenario range supported by explicit inputs. It must not be presented as an observed saving unless a real customer outcome proves it.

## 9. Success Criteria

The round-two product story is successful when a judge can answer all of the following without technical assistance:

- What business decision is being made?
- Why does the current evidence matter?
- Which framework connects evidence to the recommendation?
- What are the available strategic choices?
- What happens under each choice?
- Which financial inputs and assumptions were used?
- How large is the exposure range?
- Which sources support the conclusion?
- What uncertainty remains?
- What new event would change the recommendation?

## 10. Documentation Propagation

This file is the canonical product baseline for business-impact and decision-simulation requirements.

When implementation begins:

- POC documentation should define the minimum demonstrable subset;
- production architecture should define the scalable technical realization;
- submission material should use the business-value narrative without overstating implementation;
- slides should lead with business impact and move architecture later;
- demo scripts should show a decision changing as assumptions or evidence change.

