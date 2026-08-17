Conversion Architecture Audit

A design engineering framework for auditing how landing pages move people from first impression to meaningful action.

Most conversion advice focuses on isolated tactics: change the CTA, shorten the copy, add social proof, move pricing higher, make the button more prominent.

Conversion Architecture Audit looks at the system underneath those decisions.

It examines the order in which information is presented, what the visitor needs to understand at each point, where trust is established, when commitment is requested, what happens after the click, and whether the entire journey can actually be measured.

What it audits

The framework evaluates a landing page across:

* Narrative structure
* Information architecture
* Value proposition
* Visual hierarchy
* CTA architecture
* Commitment and friction
* Trust and proof
* Offer framing
* Responsive behavior
* Post-click continuity
* Analytics and attribution
* Full-funnel measurement

The goal isn’t to apply a fixed landing-page formula. It’s to understand the visitor’s decision sequence and design around it.

The idea

A landing page is a sequence of decisions.

At different points, a visitor is implicitly asking:

What is this?

Why should I care?

Is this relevant to me?

How does it work?

Why should I trust it?

What do I get?

What is required from me?

What should I do next?

A strong page answers those questions in an order that feels natural.

A weak page can contain all the right information and still underperform because the information appears at the wrong time.

The framework treats page order as part of conversion design.

How it works

The audit starts by establishing the primary conversion and identifying the visitor, their likely intent, acquisition source, existing knowledge, and expected level of commitment.

It then evaluates four layers of the experience.

01. Understand

Can the visitor quickly understand what is being offered and why it matters?

This includes the hero, value proposition, differentiation, copy clarity, and relevance to the visitor’s intent.

02. Progress

Does the page reveal information in an order that helps the visitor make a decision?

This includes narrative flow, section order, visual hierarchy, CTA progression, offer framing, and content density.

03. Act

Is the desired action clear, appropriately timed, and easy to complete?

This includes CTA architecture, commitment levels, friction, forms, responsive behavior, and the transition into signup, checkout, onboarding, booking, or another destination.

04. Measure

Can the team determine what actually happened?

This includes conversion events, funnel instrumentation, attribution, UTM conventions, baseline metrics, and post-click behavior.

Conversion is bigger than the landing page

A CTA click isn’t necessarily a successful conversion.

Consider:

Campaign
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

A landing page can produce an excellent click-through rate while sending users into a confusing signup flow that destroys the original intent.

For that reason, the audit follows the visitor beyond the landing page.

If someone clicks Start Free Trial, the next experience should know that they came to start a trial.

The user shouldn’t have to rediscover the action they were trying to complete.

Conversion heuristics

The framework uses ten questions throughout an audit.

Clarity
Can I explain what this page offers after a few seconds?

Relevance
Does the experience match what brought me here?

Motivation
Have I been given enough reason to continue?

Differentiation
Why should I choose this?

Momentum
Does each section make the next action feel more natural?

Trust
Do I believe the claims being made?

Friction
What might stop me?

Action
Do I know what to do next?

Continuity
Does the experience remain coherent after I click?

Measurement
Will we know whether it worked?

Audit output

A completed Conversion Architecture Audit produces five outputs.

Diagnosis

The most important conversion problems and their likely causes.

Recommended Flow

The current page structure compared with a proposed information sequence, including the reasoning behind significant changes.

Section-Level Review

Each important section is evaluated using:

Keep — what already works.

Problem — what is unclear, weak, or misplaced.

Change — what should be modified.

Why — how the recommendation improves the visitor journey.

Conversion Path

The intended journey from acquisition through successful conversion, including what happens after the primary CTA.

Measurement Plan

The events, attribution, baselines, and success criteria needed to determine whether the changes actually improved performance.

Prioritization

Not every observation deserves the same attention.

Recommendations are classified as:

P0 — Blocking

Problems that prevent conversion or damage trust, such as broken CTAs, conflicting information, incorrect pricing, placeholder content, or broken responsive layouts.

P1 — High Impact

Structural changes likely to materially improve understanding or conversion, such as page order, value proposition, CTA hierarchy, or post-click continuity.

P2 — Optimization

Improvements worth making once the fundamentals are correct, such as copy density, card layout, visual emphasis, or proof placement.

P3 — Experiment

Changes that should be tested rather than presented as universal truths, such as alternate heroes, sticky CTAs, shortened forms, or different pricing presentations.

Fundamentals come before experiments.

What this framework doesn’t do

Conversion Architecture Audit isn’t a collection of automatic CRO recommendations.

It does not assume every page needs:

* more CTAs
* bigger buttons
* testimonials
* countdown timers
* sticky banners
* shorter copy
* fewer form fields
* pricing above the fold
* popups
* artificial urgency

Those may occasionally be appropriate. They are not principles.

Every recommendation should be connected to the visitor, proposition, context, and conversion goal.

The framework also rejects manufactured scarcity, fake social proof, misleading pricing anchors, fabricated demand, and other dark patterns.

Using the skill

The complete agent instructions are available in SKILL.md.

Give the agent access to the landing page or sufficient page context, then provide the primary conversion goal and any known information about the audience or acquisition source.

The skill can be used for:

* product landing pages
* SaaS websites
* ecommerce campaigns
* waitlists
* launches
* service businesses
* marketplaces
* signup flows
* campaign pages
* pricing pages

It is most useful when the page can be inspected together with the experience that follows its primary CTA.

Why I built this

As a design engineer, I found that landing-page reviews often separated concerns that shouldn’t really be separated.

Copy would be reviewed independently from layout. Layout independently from conversion. Conversion independently from implementation. Analytics would be added after the experience had already shipped.

But these decisions affect each other.

Moving a section changes the narrative. Changing the CTA changes the expected destination. Changing the destination affects what needs to persist through signup. Running paid acquisition changes what needs to be attributed and measured.

Conversion Architecture Audit is my attempt to review those decisions as one connected system.

License

MIT
