# FACTORY_FLOOR
|| NEEDS + FIXES || 1 GLASS+HSH >> 2 WORKSHOP >> 3 LIVE >> 4 ARTIFACTS >> 5 WEBSITE >> [[NATHAN]] 


## Formal-verification intake desk | 26 October 2026

**This is an intake register, not a completed scientific showroom.** The issue descriptions below document bounded Lean mathematical checks and original-source evidence. They do not by themselves establish H(s)H physical models, new physics, measured predictions, theorem-scope completeness, or LIVE/WEBSITE publication. Preserve the original Factory Floor chain: **1 GLASS+HSH → 2 WORKSHOP → 3 LIVE → 4 ARTIFACTS → 5 WEBSITE**.

| Entry | Source / checked mathematical content | Lean CI readback | Current Factory state |
|---|---|---|---|
| [EQ-0001 / issue #2](https://github.com/Satobloc/FACTORY_FLOOR/issues/2) | Three equal sphere carrier radius identities and selected algebraic endpoint/inequality statements; **embedded regular-circle topology not fully proved in Lean** | [run 39987817298](https://github.com/Satobloc/HsH/actions/runs/39987817298): `verify` success | INTAKE / eligible for candidacy consideration only |
| [EQ-0002 / issue #3](https://github.com/Satobloc/FACTORY_FLOOR/issues/3) | Isovolumetric deformation exponential/trace identities; **constitutive dynamics not derived** | [run 39996929325](https://github.com/Satobloc/HsH/actions/runs/39996929325): `verify` success | INTAKE / mathematically checked |
| [EQ-0003 / issue #1](https://github.com/Satobloc/FACTORY_FLOOR/issues/1) | Historical filament dispersion equation **algebraic rearrangement only**, not field-action proof | [run 39960043562](https://github.com/Satobloc/HsH/actions/runs/39960043562): `verify` success | INTAKE / theory unvalidated |
| [EQ-0004 / issue #4](https://github.com/Satobloc/FACTORY_FLOOR/issues/4) | Finite-dimensional/action field Hamiltonian Legendre identities; **not a selected H(s)H action** | [run 40005392966](https://github.com/Satobloc/HsH/actions/runs/40005392966): `verify` success | INTAKE / theory unvalidated |
| [EQ-0005 / issue #5](https://github.com/Satobloc/FACTORY_FLOOR/issues/5) | Classical linear-wave/action and ring-mode algebra; **no H(s)H finite-core constitutive coefficients or held-out observable derived** | [run 40040647137](https://github.com/Satobloc/HsH/actions/runs/40040647137): `verify` success | INTAKE / theory unvalidated |

At inspection, the shared [HsH formal-verification pull request #262](https://github.com/Satobloc/HsH/pull/262) reported `open`, `merged=false`, `mergeable=false`. The individual verified issue reports identify original SAT archive source paths and committed proof variants. GitHub Actions job `verify` status was independently fetched for all five cited runs. That constitutes **CI outcome readback**, not line-by-line proof-body adjudication; do that in the WORKSHOP.

**Before a showroom/public-facing promotion:** independently open every exact Lean proof file and matching historical raw-source context; verify inputs, hypotheses, theorem statement, no hidden axioms/`sorry`, toolchain and reproducibility, external physical-data status, source/candidate separation, and editorial/presentation routing. Retain false-starts and negative gates. A finished showroom should link exact proof SHAs and explain explicitly what the theorem did *not* establish.

**Current project-return route:** [HsH Phase Steering, S04](https://github.com/Satobloc/HsH/blob/main/WORKSPACES/COMMON/PHASE_STEERING_2026-10-26.md). This is a front-door index over existing issues, not an independent assertion of theorem validity.


### Follow-up direct proof-source reading, 26 October 2026

Read all five exact source proof files from [HsH branch `infra/lean4-verification-20261023`](https://github.com/Satobloc/HsH/tree/infra/lean4-verification-20261023/FORMAL_VERIFICATION/HsHVerification):
`ArchiveEQ0001.lean` blob `12f52f9530e3d73a23f33aac99c775f2df236e91`; `ArchiveEQ0002.lean` blob `f98ef92a5f62b60818d8d78f952f23f5d2e4d8fa`; `ArchiveEQ0003.lean` blob `e126892ff8912771c7aee5da0cdd0d64f5d2fc80`; `ArchiveEQ0004.lean` blob `1726467eefab4ca44cfb7dd366069ee02660bcd3`; `ArchiveEQ0005.lean` blob `142e8ff5a037a4508b581bf146913f070e1f894d`.

**Scope audit:** All five fetched Lean sources contain theorem proofs using library tactics rather than `sorry`, new `axiom` declarations or `admit`. This is **source-code inspection** coupled to previously verified CI run outcomes; it does not establish that *every* theorem in imported Mathlib or historical source is checked here. The actual theorem statements make their needed input equations explicit as hypotheses. `EQ-0001` proves real-number radius relations, not existence of embedded intersection topology; `EQ-0002` proves real exponential identities, not finite-strain dynamics; `EQ-0003` rearranges assumed dispersion; `EQ-0004` performs finite-dimensional Legendre identities; `EQ-0005` proves assumed local balance algebra and dispersion/zero-mode identities, not Euler–Lagrange derivation, independently physical coefficients or observed data.

**First historical-source follow-up:** inspected [SAT archive `SAT O Derivations/CODE-LOCKED DERIVS.txt`](https://github.com/Satobloc/SAT_THEORY_ARCHIVE_2023-25/blob/main/SAT%20O%20Derivations/CODE-LOCKED%20DERIVS.txt) D2, lines 21–114, source blob `783b05d39d59bf854b92090e15d205e6823b51c8`. The source writes periodic `k_n=2πn/L` and `omega_n=|k_n|sqrt(T/m)`, then includes factors `1/sqrt(2*m*omega_n)` in the field-operator expansion **without an explicit `n≠0` restriction in that displayed sum**. Its `n=0` mode makes the denominator zero. Standard mathematical resolution requires excluding the zero mode from those oscillator sums or treating the constant/center-of-mass mode separately. **Mark D2 quantum-mode expansion `REQUIRES_ZERO_MODE_TREATMENT` pending full intended physical/quantum source check**, not `Lean disproved` or `physically falsified`. Related issue #5 already proves `mu≠0, mu*omega²=0 ⇒ omega=0`, but it does **not** formalize the source's singular `1/sqrt(omega)` coefficient or correct it. Distinguish `m` and linear-density `mu` as noted in existing intake.

**Next WORKSHOP test:** isolate precisely the physical 1D density and the zero-mode Hilbert-space construction; verify source derivational obligations around mode normalization and canonical commutation relations, without invented physical measurements. Any new physical calculation must meet current real-system observational-data rule. Compare with an actual known optical/condensed-matter string/wave observable only with sourced uncertainty and parameters.

This correction preserves the demonstrated formal high-water mark rather than upgrading or dismissing it.
