---
name: Conversion Architecture Audit
description: Audit landing pages and connected conversion journeys as design systems. Use for landing page audits, conversion reviews, page structure, section ordering, information architecture, value propositions, CTA hierarchy, commitment and friction, trust, responsive experience, post-click continuity, landing-page analytics, attribution, and conversion measurement across SaaS, ecommerce, marketplaces, launches, waitlists, services, campaigns, pricing pages, signup flows, and lead generation.
---

# Conversion Architecture Audit

Audit how a landing page moves a particular visitor from first impression to meaningful action. Treat narrative, interface, handoff, and measurement as one connected system.

## Core principle

A landing page is a sequence of decisions. Each section should answer the next question in the visitor’s mind:

```text
What is this?
      ↓
Why should I care?
      ↓
Is this relevant to me?
      ↓
How does it work?
      ↓
Why should I trust it?
      ↓
What do I get?
      ↓
What is required from me?
      ↓
What should I do next?
```

Treat this as a reasoning model, not a page template. Reconstruct the sequence from the audience, acquisition source, visitor awareness, proposition, conversion goal, commitment level, and product complexity.

## Required inputs

Before diagnosing, establish:

- Page URL, screenshots, source, or another complete representation of the page.
- Primary conversion and legitimate secondary actions.
- Intended visitor and their likely prior knowledge.
- Acquisition source or campaign context, if known.
- Destination after the primary CTA, including signup, checkout, lead capture, onboarding, or product access, when available.
- Existing analytics, attribution, baselines, and experiments, when available.

State what was observed directly, what was inferred, and what could not be verified. Do not present assumptions as measured facts.

## Audit workflow

### 1. Define the conversion and visitor

Name the primary conversion in one sentence. Map secondary actions and label whether they support or compete with the primary action.

Describe the visitor’s job, awareness, motivation, likely source, skepticism, and acceptable commitment. Audit for a real arrival context rather than an abstract “user.”

### 2. Reconstruct the current flow

List every meaningful section, interaction, CTA, form, and handoff in order. Include navigation, repeated CTAs, pricing, proof, FAQs, modals, redirects, and mobile-only behavior when relevant.

For every section, ask:

- What question is this trying to answer?
- What does the visitor know immediately before reaching it?
- What decision does it enable next?
- Is it early, late, redundant, or missing?

### 3. Evaluate the decision sequence

Evaluate the following dimensions together:

- **Narrative structure:** Does the story arrive in the order the visitor needs?
- **Value proposition:** Can the visitor explain the offer, outcome, and reason to choose it?
- **Information architecture:** Does information appear when it becomes useful?
- **Visual hierarchy:** Does visual weight reflect informational importance?
- **CTA architecture:** Is there a clear progression toward one primary action, with consistent language and destinations?
- **Commitment:** Is the requested effort earned by the motivation and trust already established?
- **Trust:** Does relevant evidence appear where skepticism is likely, rather than as decorative proof?
- **Friction:** What prevents continuation unnecessarily, and what friction is intentional and justified?
- **Offer framing:** Is value clear and credible without inflated anchors or hidden conditions?
- **Responsive experience:** Does hierarchy survive on mobile through wrapping, stacking, density, tap targets, and interaction changes?

Use the following diagnostic prompts throughout:

| Heuristic | Question |
| --- | --- |
| Clarity | Can I explain what this page offers after a few seconds? |
| Relevance | Does the experience match what brought me here? |
| Motivation | Have I been given enough reason to continue? |
| Differentiation | Why should I choose this? |
| Momentum | Does each section make the next action feel more natural? |
| Trust | Do I believe the claims being made? |
| Friction | What might stop me? |
| Action | Do I know what to do next? |
| Continuity | Does the experience remain coherent after I click? |
| Measurement | Will we know whether it worked? |

### 4. Follow the conversion beyond the page

Map the intended journey:

```text
Acquisition → Landing Page → Signup / Checkout / Lead Capture
           → Onboarding → Activation → Conversion → Retention
```

Inspect the primary CTA destination. Check whether the promised action, proposition, selected plan or product, campaign context, attribution, and next step survive the handoff. A CTA click is not a successful conversion if the visitor lands in a generic or contradictory experience.

Review:

- destination relevance and message continuity
- form and checkout commitment
- error states and recovery paths
- onboarding time to first meaningful value
- activation definition
- campaign and referrer persistence
- where people abandon after the click

### 5. Define measurement and attribution

Define success before recommending changes. Include:

- primary conversion and its business meaning
- secondary conversions that diagnose intent without replacing the primary goal
- funnel events such as `landing_view`, `primary_cta_click`, `signup_started`, `signup_completed`, `activation_completed`, `checkout_started`, and `conversion_completed`
- useful properties such as page variant, device, source, medium, campaign, content, referrer, and destination
- UTM naming requirements and persistence rules
- baseline metrics and measurement window
- success criteria tied to meaningful outcomes, not only click-through rate

Avoid unnecessary personal data. Analytics should answer a decision, not merely create a dashboard.

## Recommendation rules

Separate findings into:

- **Structural problems:** observed or strongly evidenced issues that should be fixed.
- **Experiments:** plausible alternatives whose impact is uncertain and must be validated.

Do not automatically recommend bigger buttons, more CTAs, shorter pages, testimonials, countdown timers, sticky CTAs, popups, fewer form fields, pricing above the fold, artificial urgency, or competitor layouts. Recommend one only when the visitor, proposition, context, implementation, or evidence justifies it.

Reject manufactured scarcity, fake social proof, fabricated reviews, misleading pricing anchors, fake demand, deceptive urgency, and dark patterns.

Prioritize:

- **P0 — Blocking:** Prevents conversion or materially damages trust. Examples: broken CTA, incorrect pricing, contradictory information, placeholder content, broken responsive layout.
- **P1 — High Impact:** Structural change likely to materially improve understanding or conversion. Examples: value proposition, section order, CTA hierarchy, post-click continuity, onboarding handoff.
- **P2 — Optimization:** Worth improving after fundamentals are correct. Examples: copy density, card layout, visual emphasis, proof placement.
- **P3 — Experiment:** Requires validation rather than universal advice. Examples: alternate hero, sticky CTA, shorter form, pricing presentation variant.

Fix fundamentals before experimenting.

## Required audit output

Produce these five outputs in order.

### 1. Diagnosis

Identify the most important conversion problems and likely causes. Focus on sequence, missing information, misplaced proof, unclear commitments, and broken handoffs rather than surface symptoms.

### 2. Recommended Flow

Show both:

```text
Current Flow: ...
Recommended Flow: ...
```

Explain why each significant move improves the visitor’s decision sequence. Do not imply that any single section has a universal location.

### 3. Section-Level Review

For each important section, use:

```text
Section: <name>
Priority: P0 / P1 / P2 / P3
Keep: <what already works>
Problem: <what is unclear, weak, or misplaced>
Change: <what to modify>
Why: <how this improves the visitor journey>
Evidence: <observation, inference, or missing verification>
```

### 4. Conversion Path

Describe the intended journey from acquisition through successful conversion and retention. Include the primary CTA destination, context carried forward, activation moment, and likely abandonment points.

### 5. Measurement Plan

Define primary and secondary conversions, funnel events, event properties, attribution requirements, baseline metrics, measurement window, and success criteria. Note any instrumentation gaps that prevent reliable conclusions.

## Final standard

The desired action should feel like the natural conclusion of the story the page has told. The visitor should not assemble the proposition alone, the interface should make hierarchy visible, the copy should make the decision understandable, the next step should be clear, the post-click experience should preserve intent, and the measurement plan should show whether the system actually worked.
