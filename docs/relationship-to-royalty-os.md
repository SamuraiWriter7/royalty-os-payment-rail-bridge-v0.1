# Relationship to Royalty OS

Royalty OS Payment Rail Bridge v0.1 is positioned after the allocation logic
of Royalty OS.

It does not replace Royalty OS.

It extends Royalty OS toward external value circulation.

---

## 1. Purpose

The purpose of this document is to define the relationship between Royalty OS
and the Payment Rail Bridge.

Royalty OS defines how value should be recognized, traced, evaluated,
and allocated.

The Payment Rail Bridge defines how allocation intent may be translated into
external payment circulation.

```text
Royalty OS = allocation logic
Payment Rail Bridge = circulation interface
External Payment Rail = settlement channel
```

The bridge exists because allocation logic and payment execution should remain
separate layers.

---

## 2. Position in the Stack

Royalty OS Payment Rail Bridge sits downstream of the core Royalty OS layers.

```text
Origin Detection
        ↓
Trace Layer
        ↓
Impact / Seismic Score
        ↓
Allocation Readiness
        ↓
Royalty OS
        ↓
Payment Rail Bridge
        ↓
External Payment Rail
        ↓
Recipients
```

This means that the bridge should only operate after trace, scoring,
and allocation-readiness processes have prepared sufficient context.

---

## 3. Royalty OS Responsibilities

Royalty OS is responsible for value recognition and allocation logic.

Its responsibilities may include:

- identifying value sources
- preserving trace references
- evaluating influence or contribution
- defining allocation rules
- preparing recipient mappings
- recording review status
- preserving dispute awareness
- distinguishing contribution from ownership
- preventing premature automatic payment

Royalty OS does not need to execute payments directly.

Its role is to define why value should flow, to whom, and under what conditions.

---

## 4. Payment Rail Bridge Responsibilities

The Payment Rail Bridge is responsible for translating Royalty OS allocation
logic into payment-compatible instructions.

Its responsibilities may include:

- converting allocation intent into settlement instructions
- preserving trace metadata
- preserving allocation references
- mapping recipients to payment-compatible identities
- preparing payment intent
- attaching review status
- attaching dispute status
- receiving settlement status from external rails
- preventing payment rail lock-in

The bridge should not decide value by itself.

It should carry forward the decision context prepared by Royalty OS.

---

## 5. External Payment Rail Responsibilities

External payment rails are responsible for value movement.

They may include:

- wallet systems
- P2P payment networks
- card-based settlement systems
- bank transfer systems
- stablecoin rails
- micropayment systems
- platform-native payment systems
- agent-native payment protocols
- XMoney as one possible candidate

External payment rails may execute or represent settlement.

However, they do not define the origin, trace, or allocation logic of value.

---

## 6. Layer Separation

The architecture depends on clear separation between recognition, allocation,
and circulation.

```text
Recognition → Allocation → Circulation
```

These layers should not be collapsed into one another.

A payment rail should not determine contribution.

A score should not automatically execute payment.

A trace record should not become a legal judgment by itself.

Royalty OS should remain responsible for allocation logic.

Payment rails should remain responsible for circulation.

The bridge should preserve context between them.

---

## 7. Why Separation Matters

Separation matters because value circulation can become dangerous if context
is lost.

Without trace, payment becomes blind transfer.

Without review, scoring may become automatic enforcement.

Without dispute paths, mistaken allocation becomes difficult to correct.

Without payment rail neutrality, Royalty OS may become dependent on one provider,
platform, currency, or jurisdiction.

The Payment Rail Bridge exists to prevent these failures.

---

## 8. Payment Rail Neutrality

Royalty OS should remain payment-rail-neutral.

This means:

- Royalty OS should not depend on XMoney alone.
- Royalty OS should not depend on any single wallet provider.
- Royalty OS should not depend on any single platform.
- Royalty OS should not depend on any single currency.
- Royalty OS should be able to connect to multiple payment rails through bridges.

XMoney may be treated as one possible payment-rail candidate.

It should not be treated as the required or official payment layer of Royalty OS.

---

## 9. Allocation Intent

The core object passed from Royalty OS to the Payment Rail Bridge is not money.

It is allocation intent.

Allocation intent may include:

- allocation ID
- trace reference
- origin reference
- recipient reference
- contribution description
- allocation amount or share
- confidence level
- review status
- dispute status
- payment eligibility
- settlement constraints

The bridge may then translate this intent into a payment-rail-compatible form.

---

## 10. Trace Preservation

Every allocation-to-payment flow should preserve trace context.

Trace context may include:

- source reference
- structure fingerprint reference
- communication trace reference
- lineage reference
- signed impact attestation reference
- dispute registry reference
- allocation readiness reference

This does not require all trace data to be public.

It requires that payment flows remain accountable.

---

## 11. Dispute Awareness

The Payment Rail Bridge should preserve dispute awareness.

Possible dispute states may include:

- no dispute
- under review
- contested
- blocked
- suspended
- resolved
- reversed
- superseded

If an allocation is disputed, the bridge should not erase that status.

A payment rail may not understand all dispute logic internally.

Therefore, the bridge must preserve dispute metadata before, during,
and after circulation.

---

## 12. Relationship to Allocation Readiness

Allocation Readiness acts as the gate before Royalty OS value circulation.

It asks whether a claim or allocation is ready to move forward.

The Payment Rail Bridge should respect this layer.

```text
Allocation Readiness
        ↓
Royalty OS
        ↓
Payment Rail Bridge
```

If allocation readiness is incomplete, blocked, or disputed, the bridge should
not treat the allocation as fully payment-ready.

---

## 13. Relationship to Trace Architecture

Trace Architecture provides the memory of value.

It records how influence, reference, access, communication, or structural impact
moves through a system.

Royalty OS uses trace architecture to support allocation decisions.

Payment Rail Bridge preserves references to those traces when value begins to flow.

```text
Trace Architecture → Royalty OS → Payment Rail Bridge
```

Without trace architecture, payment circulation loses its memory.

---

## 14. Relationship to Seismic / Impact Scoring

Seismic or Impact Scoring evaluates the strength of contribution or influence.

However, scores should not directly trigger payment.

Scores should pass through readiness, review, and allocation logic.

```text
Score → Readiness → Royalty OS → Bridge → Payment Rail
```

This prevents raw metrics from becoming automatic financial enforcement.

---

## 15. Relationship to the Five Elements Model

In the Five Elements Value Circulation Model, Royalty OS belongs mainly to
the Metal layer.

Payment Rail Bridge sits between Metal and Water.

```text
Metal = scoring, allocation, value crystallization
Bridge = translation from allocation to circulation
Water = payment rails, liquidity, settlement
```

The bridge is therefore the transition point where crystallized value becomes
circulating value.

---

## 16. Minimal Bridge Contract

A minimal bridge contract should preserve the following fields:

```yaml
allocation_intent:
  allocation_id: string
  origin_reference: string
  trace_reference: string
  recipient_reference: string
  allocation_value:
    type: share | amount | points | credits | other
    value: number
    unit: string
  review_status: pending | approved | blocked | disputed | resolved
  dispute_status: none | contested | suspended | resolved
  payment_eligibility: eligible | not_eligible | pending_review
  payment_rail_candidate: string
  settlement_status: pending | completed | failed | blocked | reversed
```

This is not a final schema.

It is a conceptual bridge contract.

---

## 17. Non-Goals

This relationship does not imply that the Payment Rail Bridge:

- replaces Royalty OS
- executes legal payment by itself
- determines legal ownership
- bypasses compliance or KYC
- removes human or multi-agent review
- converts every influence signal into payment
- depends on XMoney as the only rail
- removes dispute or correction paths

The bridge exists to connect layers, not collapse them.

---

## 18. Civilizational Role

Royalty OS is the nervous system.

It detects, evaluates, and allocates.

Payment rails are the bloodstream.

They circulate value.

The Payment Rail Bridge is the interface between them.

```text
Nervous System → Circulation Interface → Bloodstream
```

This relationship allows value to move without losing memory.

It allows money to circulate without becoming blind.

It allows creators, agents, platforms, and communities to receive value
while preserving trace and accountability.

---

## 19. Summary

Royalty OS Payment Rail Bridge v0.1 extends Royalty OS toward external
value circulation.

Royalty OS defines why value should flow.

The Payment Rail Bridge defines how that allocation intent can be translated
into payment-compatible instructions.

External payment rails define where and how settlement may occur.

```text
Royalty OS defines value logic.
Payment Rail Bridge preserves and translates that logic.
Payment rails circulate value.
```

The goal is not simply payment.

The goal is trace-aware, review-aware, dispute-aware value circulation.
