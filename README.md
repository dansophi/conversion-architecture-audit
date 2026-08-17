# Conversion Architecture Audit

**An open-source design engineering framework for auditing how landing pages move people from first impression to meaningful action.**

Audit narrative structure, information hierarchy, value proposition, visual hierarchy, CTA progression, trust, friction, post-click continuity, analytics, and attribution as one connected system.

Designed to be used by both humans and AI agents.

> A landing page is a sequence of decisions. Every section should answer the next question in the visitor's mind.

## Why this exists

Most landing page advice focuses on isolated tactics:

- Make the CTA bigger
- Shorten the copy
- Add testimonials
- Move pricing higher
- Add urgency
- Reduce form fields

Those changes can help. They can also completely miss the problem.

A page can have strong copy, polished visuals, a prominent CTA, and all the expected sections and still convert poorly because the underlying sequence is wrong.

**Conversion Architecture Audit looks at the system underneath the page.**

It asks whether visitors receive the right information, in the right order, with enough motivation and trust to take the next action.

Then it follows that action beyond the landing page to determine whether the experience actually completes the conversion.

---

## What it audits

The framework evaluates:

**Narrative**  
Does the page tell its story in the right order?

**Value proposition**  
Can visitors quickly understand what is being offered and why it matters?

**Information architecture**  
Does information appear when visitors actually need it?

**Visual hierarchy**  
Does visual weight match informational importance?

**CTA architecture**  
Is there a clear progression toward the primary action?

**Trust**  
Does evidence appear where skepticism is likely to occur?

**Friction**  
What might unnecessarily prevent someone from continuing?

**Post-click continuity**  
Does the experience after the CTA preserve the visitor's original intent?

**Measurement**  
Can the team determine where conversion succeeds or fails?

**Attribution**  
Can acquisition be connected to meaningful outcomes?

---

## The model

At different points in a landing page, a visitor is implicitly asking:

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

The exact order changes depending on the product, visitor, acquisition source, existing awareness, and level of commitment.

The framework does not prescribe a universal landing page template.

It reconstructs the decision sequence first, then evaluates the page against it.

---

## Example

Imagine a product landing page currently structured like this:

```text
Hero
  ↓
Feature Grid
  ↓
Integrations
  ↓
Technical Details
  ↓
Pricing
  ↓
Testimonials
  ↓
CTA
```

Nothing is necessarily wrong with any individual section.

The problem may be the sequence.

The page asks visitors to understand features and implementation before establishing why the product matters or providing evidence that it works.

An audit might instead recommend:

```text
Hero
  ↓
Core Outcome
  ↓
How It Works
  ↓
Proof
  ↓
Key Capabilities
  ↓
Integrations
  ↓
Pricing
  ↓
FAQ
  ↓
CTA
```

The recommendation isn't:

> Testimonials always belong above features.

It is:

> Establish the outcome, explain the mechanism, and resolve the visitor's likely trust question before asking them to evaluate detailed capabilities.

That distinction is the point of the framework.

---

## It doesn't stop at the CTA

A CTA click is not necessarily a successful conversion.

```text
Acquisition
     ↓
Landing Page
     ↓
Signup
     ↓
Onboarding
     ↓
Activation
     ↓
Conversion
     ↓
Retention
```

A landing page can produce an excellent click-through rate while sending users into a signup or onboarding experience that destroys the original intent.

Conversion Architecture Audit follows the visitor through that handoff.

If someone clicks **Start Free Trial**, the next experience should understand that they came to start a trial.

The visitor should not have to rediscover what they were trying to do.

---

## What an audit produces

A completed audit returns five things.

### 1. Diagnosis

The highest-impact conversion problems and their likely causes.

### 2. Recommended Flow

The existing information sequence compared with a proposed structure, including the reasoning behind significant changes.

### 3. Section-Level Review

Each important section is evaluated using:

**Keep** — what already works  
**Problem** — what is unclear, weak, or misplaced  
**Change** — what should be modified  
**Why** — how the recommendation improves the visitor journey

### 4. Conversion Path

The intended journey from acquisition through successful conversion, including what happens after the primary CTA.

### 5. Measurement Plan

The events, attribution, baselines, and success criteria required to determine whether the changes actually improved performance.

---

## Priority system

Recommendations are classified by impact rather than presented as an undifferentiated list.

**P0 · Blocking**

Problems that prevent conversion or damage trust.

Examples: broken CTAs, incorrect pricing, conflicting information, placeholder content, broken responsive layouts.

**P1 · High Impact**

Structural changes likely to materially improve understanding or conversion.

Examples: value proposition, page order, CTA hierarchy, post-click continuity.

**P2 · Optimization**

Improvements worth making after the fundamentals are correct.

Examples: copy density, card layout, visual emphasis, proof placement.

**P3 · Experiment**

Changes that require evidence rather than assumptions.

Examples: alternate heroes, sticky CTAs, shortened forms, different pricing presentations.

**Fix fundamentals before experimenting.**

---

## Conversion heuristics

The framework uses ten questions throughout an audit:

| | Question |
|---|---|
| **Clarity** | Can I explain what this page offers after a few seconds? |
| **Relevance** | Does the experience match what brought me here? |
| **Motivation** | Have I been given enough reason to continue? |
| **Differentiation** | Why should I choose this? |
| **Momentum** | Does each section make the next action feel more natural? |
| **Trust** | Do I believe the claims being made? |
| **Friction** | What might stop me? |
| **Action** | Do I know what to do next? |
| **Continuity** | Does the experience remain coherent after I click? |
| **Measurement** | Will we know whether it worked? |

These are diagnostic prompts, not rigid rules.

---

## What it won't automatically tell you to do

This isn't a checklist of CRO clichés.

The framework does not automatically recommend:

- more CTAs
- larger buttons
- testimonials
- countdown timers
- sticky banners
- shorter pages
- fewer form fields
- pricing above the fold
- popups
- artificial urgency

Any of those may be appropriate.

None of them are universally correct.

Every recommendation should be connected to the visitor, proposition, context, and conversion goal.

The framework also rejects manufactured scarcity, fake social proof, misleading pricing anchors, fabricated demand, and other dark patterns.

---

## Use it as an Agent Skill

The full agent instructions live in [`SKILL.md`](./SKILL.md).

The skill is designed around the open `SKILL.md` format so it can be used in compatible agent workflows rather than existing only as a static checklist.

Give the agent:

1. The landing page, screenshots, or sufficient page context
2. The primary conversion goal
3. Any known audience context
4. Acquisition sources, if known
5. Access to the post-click experience when possible

Then ask it to run a Conversion Architecture Audit.

For example:

```text
Audit this landing page using Conversion Architecture Audit.

Primary conversion: Start free trial
Audience: Small product teams
Primary acquisition: Organic search and paid social

Inspect the complete page and the experience after the primary CTA.

Prioritize structural conversion problems before optimizations.
```

The skill can be applied to:

- SaaS
- ecommerce
- product launches
- marketplaces
- service businesses
- waitlists
- campaign pages
- signup flows
- pricing pages
- lead generation

---

## Repository structure

```text
conversion-architecture-audit/
├── README.md
├── SKILL.md
├── examples/
│   └── example-audit.md
└── assets/
    └── preview.png
```

`README.md` explains the methodology.

`SKILL.md` contains the executable audit instructions.

`examples/` demonstrates what a completed audit should look like.

`assets/` contains supporting visuals and diagrams.

---

## Why I built it

Landing page reviews often separate decisions that are tightly connected.

Copy gets reviewed independently from layout.

Layout gets reviewed independently from conversion.

Conversion gets reviewed independently from implementation.

Analytics gets added after the experience has already shipped.

But those decisions affect each other.

Moving a section changes the narrative.

Changing a CTA changes the expected destination.

Changing the destination affects what needs to persist through signup.

Changing the acquisition strategy affects what needs to be attributed and measured.

As a design engineer, I wanted a framework that treats those decisions as one connected system.

**Conversion Architecture Audit is that framework.**

---

## Contributing

Ideas, improvements, examples, and edge cases are welcome.

If you use the framework on a different type of landing page and find something the current audit does not account for, open an issue or submit a pull request.

The goal is to make the methodology more useful without turning it into a collection of generic conversion rules.

---

## License

MIT

---

If this framework is useful in your work, consider starring the repository. It helps other designers, engineers, founders, and agent builders discover it.
