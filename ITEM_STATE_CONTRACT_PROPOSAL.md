# Factory Floor Item State Contract (proposal)

**Status:** PROPOSAL / NON-OPERATIVE UNTIL REVIEWED  
**Purpose:** implement FF-002 without replacing existing source or equation registries.

## Design decision

Use a **thin lifecycle envelope** around each canonical research artifact. The envelope tracks where an item is in the wider research system; the source repository remains the home of the actual equation, proof, calculation, paper, image, or conversation.

This avoids creating a competing equation database. In particular:

- HsH `formalization/schema/equation.schema.json` remains the equation-specific registry schema.
- HsH `WORKSPACES/COMMON/EQUATION_INTAKE_0001_LANE_REGISTER_2026-10-23.md` remains a source/equation intake record.
- HsH `BEDROCK.md` remains theory-premise authority.
- Factory Floor owns cross-repository workflow state and the process record, not theory truth.
- Existing IDs such as `EQ-0001` should be retained; the envelope points to canonical source records rather than renumbering them.

## Independent status dimensions

Do not collapse these into one status field:

| Dimension | Question answered | Example |
|---|---|---|
| `theory_status` | What is this item's relationship to current H(s)H? | `sandbox` |
| `workflow_status` | Where is it in the intake/review/promotion process? | `ci_passed` |
| `math_status` | What mathematical work has actually been completed? | `lean_checked` |
| `physical_status` | What empirical standing does it have? | `no_prediction` |
| `presentation_status` | Is there an approved reader-facing derivative? | `source_only` |
| `visibility` | Who may see it? | `internal` |

A single object may validly be `theory_status=sandbox`, `math_status=lean_checked`, `physical_status=no_prediction`. That is not a contradiction.

## Provenance and authorship

Each source reference records repository, path, source role and, when available, commit/blob SHA, locator, author/speaker and date. Distinguish Nathan Direct, historical author, assistant-generated reconstruction, external source, mixed authorship and unresolved attribution.

Do not infer Nathan's intent from a generated summary. Apply the HsH Original-Statement-First Research Gate before substantive theory work.

## Promotion semantics

- `ci_passed` means the recorded CI job succeeded. It is not mathematical clearance.
- `workshop_cleared` is reserved for a bounded mathematical review of source fidelity, assumptions, derivation, proof, dimensions, signs, limits, topology and reproducibility.
- `eligible_for_candidacy_consideration` is the maximum implication of Factory Floor mathematical clearance. It is not an H(s)H candidate.
- `incorporated` requires an explicit Nathan-authorized construction decision and a versioned HsH destination.
- Physical assessment is an independent axis. No previous state implies physical validation.

## BEDROCK constraints

- Real observational/experimental systems and data are the default for physical calculations.
- Data-free calculations, including pure-geometry and numerical-fixture calculations, require Nathan's explicit prior permission.
- Preserve historical source equations and corrections; do not silently normalize or overwrite conflicting versions.
- A failed or unresolved result remains a durable record, not a deleted row.

## Schema

The companion JSON Schema is `schemas/floor_item.schema.json`. It validates the envelope only. It intentionally does not attempt to validate LaTeX, Lean proof correctness, physical data, or theory adoption.

## Migration plan

1. Review this contract and schema.
2. Map existing Factory Floor EQ records to envelopes without changing their current statuses.
3. Link to existing HsH equation entries and Lean source/CI artifacts; do not duplicate equation bodies.
4. Add non-equation objects only after the ID namespace and ownership are agreed.
5. Validate records and check referential integrity before enabling automation.
6. Keep all migration changes reversible and source-linked.

## Not yet done

No existing item has been migrated, no status has been changed, and no automation consumes this schema. This proposal is not an adoption decision.
