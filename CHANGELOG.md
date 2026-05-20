# Changelog

All notable changes to this repository will be documented in this file.

---

## v0.1.1 - Examples and Future Extensions

Added explanatory roadmap and sample flow files to clarify how the v0.1 architecture may evolve toward future implementation layers.

Added:

- `docs/future-extensions.md`
- `examples/allocation-intent.sample.yaml`
- `examples/xmoney-candidate-flow.sample.yaml`

Updated:

- `README.md`
  - Added `docs/future-extensions.md` to Repository Structure
  - Added `examples/` directory to Repository Structure
  - Added Start Here guidance for future extensions and examples
  - Updated Status from conceptual architecture to conceptual architecture with examples

Clarified:

- Future extension direction toward Royalty Event Layer
- Allocation Intent Schema as a possible v0.2 direction
- Payment Rail Candidate Profile as a possible v0.2 direction
- Bridge Lifecycle Model as a possible future layer
- Validation and CI as a possible v0.3 direction
- Agent-native payment interface as a possible v0.4 direction
- Payment rail interface profiles as a possible v0.5 direction

Added sample objects for:

- allocation intent before payment rail translation
- XMoney as one possible Water-layer payment rail candidate
- bridge translation context
- recipient mapping placeholder
- settlement status placeholder
- dispute and review preservation
- safety notes for non-production use

Status:

- Version: v0.1.1
- Specification: v0.1.0
- Maturity: Conceptual architecture with examples
- Scope: Specification draft, roadmap, and sample flows

---

## v0.1.0 - Draft

Initial draft release of Royalty OS Payment Rail Bridge v0.1.

Added:

- `README.md`
- `spec/payment-rail-bridge-v0.1.yaml`
- `docs/architecture-overview.md`
- `docs/five-elements-value-circulation-model.md`
- `docs/xmoney-as-payment-rail-candidate.md`
- `docs/relationship-to-royalty-os.md`
- `diagrams/royalty-os-payment-rail-bridge.dot`
- `diagrams/five-elements-value-circulation.dot`
- `CITATION.cff`
- `LICENSE`

Defined:

- Royalty OS as the value allocation logic layer
- Payment Rail Bridge as the circulation interface
- External payment rails as downstream settlement channels
- XMoney as one possible payment-rail candidate
- Five Elements Value Circulation Model
- Trace-aware, review-aware, dispute-aware value circulation principles

Status:

- Version: v0.1.0
- Maturity: Conceptual architecture
- Scope: Draft specification
