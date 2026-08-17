# Example Audit: Northstar Relay

Northstar Relay is a fictional SaaS product for small operations teams. It turns recurring customer requests from email and chat into a shared queue with owners, due dates, and a lightweight status view.

This example is intentionally compact. It demonstrates reasoning through a page rather than applying a universal section checklist.

## Context

- **Primary conversion:** Start a 14-day free trial
- **Visitor:** Operations lead at a 10–40 person company who currently coordinates requests in shared inboxes and spreadsheets
- **Primary acquisition:** Search for “shared customer request tracker” and retargeting ads
- **Likely awareness:** Problem-aware; comparing practical alternatives, not looking for a category definition
- **Commitment:** Medium; account creation is acceptable, but payment and implementation effort are not yet earned

## Current page flow

```text
Hero → logo strip → feature grid → integrations → pricing → customer story
     → FAQ → Start free trial CTA → generic account creation
```

The hero says “Operations, aligned.” The supporting copy describes “a modern command center for teams.” The primary CTA says “Get started.”

## Diagnosis

### P1 — The page explains the category before the outcome

The visitor already knows they need a better request-tracking workflow. The hero uses abstract language, while the concrete outcome appears only in the feature grid. This forces the visitor to translate the product into their own problem before they know whether it is relevant.

### P1 — The CTA does not preserve the promise

“Get started” is ambiguous and leads to a generic account screen with no selected use case or trial context. The page asks for an account before showing what the first session will accomplish. This weakens momentum after the click.

### P2 — Proof arrives after the commitment decision

The customer story is useful, but it follows pricing. Search visitors are likely to ask whether Relay is credible for a small team before evaluating plan details. The proof should resolve that concern nearer to the outcome and workflow explanation.

### P2 — Technical detail is not connected to the decision

Integrations are presented as a logo grid. The page does not explain which workflow each integration supports or whether a team can start without changing its existing tools.

### P3 — Pricing and CTA presentation need validation

A single plan comparison is not obviously wrong. Testing annual emphasis or a persistent CTA should wait until the proposition and handoff are clear.

## Recommended page flow

```text
Hero: concrete outcome + Start free trial
  ↓
Who it is for / problem context
  ↓
How it works: capture → assign → resolve
  ↓
Relevant customer proof
  ↓
Capabilities mapped to the workflow
  ↓
Integrations with “keep your current tools” explanation
  ↓
Pricing, trial terms, and implementation effort
  ↓
FAQ: migration, permissions, security, cancellation
  ↓
Final CTA with the same trial language
```

The sequence answers relevance and mechanism before asking the visitor to compare detail. Proof moves before capability depth because the likely question is “Will a team like mine actually use this?” Pricing remains available once the offer is understood, rather than being hidden or forced above the fold.

## Section-level review

### Hero

- **Priority:** P1
- **Keep:** Direct access to the trial and a compact product visual.
- **Problem:** “Operations, aligned” does not name the job Relay performs; “Get started” does not set an expectation.
- **Change:** Lead with “Turn scattered customer requests into an owned queue your team can clear.” Change the CTA to “Start 14-day free trial” and state whether a card is required.
- **Why:** The visitor can test relevance and understand the commitment without inference.

### Logo strip

- **Priority:** P2
- **Keep:** It can establish that the product is used by real teams.
- **Problem:** Logos alone do not prove fit and currently interrupt the explanation before the mechanism.
- **Change:** Move or reduce it; pair any retained proof with a specific outcome or customer segment.
- **Why:** Evidence should answer a concern, not consume attention as decoration.

### Feature grid

- **Priority:** P1
- **Keep:** The underlying capabilities are relevant.
- **Problem:** Features are not mapped to the visitor’s workflow, so the visitor must assemble the mechanism.
- **Change:** Replace the grid with three steps: capture requests, assign ownership, close the loop. Attach capabilities to each step.
- **Why:** The page demonstrates how the promise becomes an operational result.

### Integrations

- **Priority:** P2
- **Keep:** Existing-tool compatibility is a meaningful objection reducer.
- **Problem:** A logo grid does not say whether setup requires migration.
- **Change:** Explain the first useful integration path and what remains unchanged.
- **Why:** It converts technical detail into a lower-risk implementation story.

### Pricing

- **Priority:** P2
- **Keep:** Pricing is visible before the final action.
- **Problem:** Trial terms and cancellation conditions are not prominent enough to establish the real commitment.
- **Change:** State plan limits, trial duration, payment requirement, and cancellation plainly; retain variants as experiments.
- **Why:** Transparent commitment reduces avoidable hesitation and protects trust.

### Final CTA and account creation

- **Priority:** P1
- **Keep:** The page has a clear place to act.
- **Problem:** The CTA label changes from the promise, and the destination is generic.
- **Change:** Pass the trial intent, selected plan, campaign parameters, and source context into account creation; show the first task after signup.
- **Why:** The visitor should continue the action they chose rather than restart the decision.

## Conversion path

```text
Search / retargeting ad
  → request-tracker landing page
  → Start 14-day free trial
  → account creation with trial context
  → connect inbox or paste first request
  → assign an owner and resolve one request
  → activation: first request marked resolved
  → paid conversion after trial
  → retained weekly workflow
```

The first session should make the promised outcome tangible. If a visitor clicks from a campaign about shared inboxes, preserve that source and show the inbox connection path first. Do not drop them into an empty generic dashboard.

## Priorities

| Priority | Finding | Next action |
| --- | --- | --- |
| P0 | No blocking defect observed in the supplied page review. Verify trial and billing states before release. | Test CTA, pricing, form errors, and mobile layout end to end. |
| P1 | Abstract proposition; capabilities precede mechanism; generic post-click handoff. | Rewrite hero, reorder flow, and carry trial intent into signup. |
| P2 | Uncontextualized logos and integrations; unclear trial terms. | Attach evidence to objections and make commitment explicit. |
| P3 | Alternate hero, sticky CTA, annual-plan emphasis. | Test only after P1 changes are instrumented. |

## Measurement plan

### Primary conversion

`trial_activated`: a new account connects a source, creates or imports a request, and marks one request resolved within seven days.

### Secondary conversions

- `primary_cta_click`
- `signup_started`
- `signup_completed`
- `integration_started`
- `first_request_created`
- `first_request_resolved`
- `pricing_viewed`
- `paid_conversion`

### Required properties

Persist `utm_source`, `utm_medium`, `utm_campaign`, `utm_content`, referrer, device class, page variant, selected plan, and landing-page intent through signup and trial activation. Do not send message content or unnecessary personal information.

### Baseline and success criteria

Record the current baseline for CTA click-through, signup completion, activation within seven days, paid conversion, and week-four retention by acquisition source and device. The first release succeeds if activation rate improves without reducing qualified paid conversion or retention. Treat CTA click-through as a diagnostic step, not the final success metric.
