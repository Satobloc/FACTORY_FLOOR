# GEOMETRY-FIRST ADMISSION GATE — PROPOSAL
**Repository:** Satobloc/FACTORY_FLOOR  
**Status:** PROPOSAL ONLY — NON-OPERATIVE PENDING NATHAN REVIEW  
**Authority:** Proposed workflow admission rule. Does not amend H(s)H BEDROCK or alter existing item status.  
**Date:** 2026-11-03

## 1. Governing rule

**No item enters Factory Floor unless its system-under-study is represented by a precise geometric plot, the plot has passed documented hostile fidelity review, and the reviewed plot is displayed with the item.**

This applies to all Factory Floor intake, not merely items classified as geometry papers or figures. It applies to equations, derivations, Lean results, simulations, software, claims, research packets, reviews, and papers whenever they describe, assume, constrain, derive from, or make a point about a geometric form or relation.

The project's geometric claims are not self-interpreting. A sentence, symbol, equation, or proof that refers to a geometric object must identify what that object is. The plot is part of the scientific object and its evidence trail, not decoration added after the mathematics.

**If the geometry is wrong, ambiguous, under-specified, or disconnected from the mathematics, the associated mathematical result is uncoupled, unnecessary, or irrelevant to the claimed system until the mismatch is resolved.**

No algebraic manipulation, numerical result, simulation, Lean proof, elegance, or paper polish can waive this gate.

## 2. Scope: what must be plotted

The gate applies whenever an item invokes any of the following, whether explicitly or implicitly:

- points, trajectories, worldlines, worldtubes, worldvolumes, surfaces, sheets, wavefronts, timesheets, cross-sections, boundaries, normals, frames, axes, coordinates, or embeddings;
- curvature, torsion, winding, linking, braiding, twisting, intersections, separation, adjacency, topology, orientation, chirality, or handedness;
- fields, flows, media, filaments, vortices, coils, rings, cores, carriers, modes, deformations, or interactions;
- geometric limits, approximations, projections, mappings, transformations, or dimensional reductions;
- any paper claim whose meaning depends on the shape, location, orientation, connectivity, scale, or relation of physical or mathematical objects.

A plot must depict the system at the level needed to understand the claim. A schematic may help orient the reader, but cannot substitute for a precise plot where a precise geometric object is claimed.

## 3. Required admission packet

Every proposed Floor item must carry the following together as one inspectable packet:

1. **Geometric plot**
   - A visible, legible plot of the actual system-under-study at the level of the claim.
   - The plot is stored as a durable artifact and displayed inline/on the item page, not merely linked to an undisplayed file.
   - If multiple views are necessary to disambiguate the object, include them as a coordinated figure set.
   - A generic stock image, decorative illustration, unexplained rendering, or unlabeled doodle does not qualify.

2. **Geometric specification**
   - Explicit identification of objects, dimensions, coordinate system, units, orientation, topology, boundaries, scale, and relevant relations.
   - State which features are exact, assumed, measured, fitted, idealized, schematic, or conjectural.
   - Identify the equations/claims represented by each plotted feature.
   - State what the plot does not represent.
   - Include source and version/commit identity for the underlying construction, geometry data, script, and rendered image.
   - Include the rendering method and all parameters needed to reproduce the plot.

3. **Claim-to-geometry correspondence**
   - A mapping from each geometry-dependent claim/equation/theorem to the particular plotted objects, features, relations, and assumptions it uses.
   - Explain how symbols and variables correspond to visible geometric elements.
   - Identify any mathematical structure not visible in the plot and justify why it is omitted.
   - Explicitly flag any point at which the derivation abstracts away from, idealizes, or changes the plotted system.

4. **Hostile fidelity review**
   - A review by someone or some independently executed review process not responsible for producing the plot.
   - Review must attempt to falsify whether the plot faithfully represents the stated system and whether the geometry actually supports the associated equations and claims.
   - Review must test for missing dimensions, incorrect topology, hidden intersections, misleading projections, coordinate/frame errors, scale distortions, wrong orientation/handedness, omitted boundaries, inconsistent assumptions, and visual features unsupported by source or construction.
   - Review records reviewer identity/role, exact plot and specification hashes/commit identities, review date, objections, tests performed, and disposition of each objection.
   - A self-check, author assertion, automated render success, or unreasoned approval is not hostile review.

5. **Co-located display**
   - The reviewed plot, its specification, and the hostile-review disposition must be displayed with the item wherever the item is presented inside Factory Floor.
   - The reader must not need to chase a separate repository or conversation to discover what geometry is being discussed.
   - The display must preserve visible review status and any unresolved limitations.

## 4. Geometry fidelity review states

Use explicit states; do not collapse them into a single green check:

- **GEOMETRY_NOT_SUPPLIED** — no qualifying plot/specification.
- **GEOMETRY_INCOMPLETE** — plot exists but required geometric facts or claim mapping are missing.
- **GEOMETRY_REVIEW_PENDING** — packet is complete enough to review; independent hostile review has not concluded.
- **GEOMETRY_REJECTED** — hostile review found a material fidelity defect or unresolved contradiction.
- **GEOMETRY_REPAIR_REQUIRED** — objections require correction and a new plot/review cycle.
- **GEOMETRY_FIDELITY_CLEARED** — hostile review found the plot faithful to the declared system and scope, with limitations recorded.
- **GEOMETRY_FIDELITY_CLEARED_WITH_LIMITATIONS** — plot is faithful only within explicitly bounded scope; the limitations remain displayed.
- **GEOMETRY_NOT_APPLICABLE** — allowed only by a documented reviewer-approved argument that the item makes no geometric claim, invokes no geometric object or relation, and depends on no geometric assumptions. This exception should be rare in H(s)H.

Only the two fidelity-cleared states satisfy the geometry gate. A conditional clearance does not authorize claims outside its stated scope.

## 5. Admission sequence and hard stop

The proposed sequence is:

**source item → geometric specification → precision plot → claim-to-geometry map → hostile fidelity review → co-located display check → Factory Floor admission decision**

Before admission:
- assign no active Factory Floor stage beyond a quarantined/pre-intake holding record;
- do not count the item as Floor intake, WORKSHOP, LIVE, ARTIFACT, or WEBSITE material;
- do not let Lean success, CI success, or paper acceptance substitute for this gate;
- preserve the item and its provenance in its source repository while blocked;
- record the exact reason for the block and the smallest corrective action.

After geometry clearance, the item still requires all other applicable source, mathematical, physical, theory-status, privacy, licensing, and presentation gates. Geometry clearance means only that the depicted geometry faithfully represents the declared system within the reviewed scope. It does not certify the equations, prove the theory, validate the physical model, or establish observational agreement.

## 6. Existing items and papers

This proposal does not retroactively change the status of any existing Factory Floor entry. It does require a geometry-gate audit before any existing item is advanced, repackaged, or newly presented as Floor material under the proposed rule.

For papers:
- every geometry-dependent central claim must have a corresponding precise plot;
- every figure must have a defined evidentiary role and geometric specification;
- hostile review must test the geometry against the paper's definitions, equations, and conclusions;
- a paper's prose, equations, and figures must agree about the same system;
- a paper cannot pass this gate by adding a decorative overview image while leaving the actual claimed construction unplotted.

## 7. Visual classes and implementation

The existing Factory Floor visual taxonomy remains useful but must be interpreted under this gate:

- **P — precision/script-drawn:** preferred for geometry evidence; script and parameter manifest are required.
- **H — controlled hybrid:** acceptable only when the scientifically relevant geometry remains exact, traceable, and independently reviewable. Identify which components are generated, measured, manually composed, or illustrative.
- **I — illustrative:** orientation or communication aid only; never sufficient for geometry fidelity clearance.

For a plot to qualify as precision evidence, its source data/construction and rendering script must be retained. The image alone is not enough. A static image can be displayed, but the underlying geometry and rendering procedure must remain inspectable.

## 8. Minimum hostile-review checklist

Reviewers must answer, with evidence:

1. What exact geometric system is depicted?
2. Are the dimensions, coordinate frame, units, orientation, and scale explicit and internally consistent?
3. Does the plotted topology match the stated topology?
4. Are all relevant boundaries, intersections, separations, links, twists, and connections represented correctly?
5. Does the projection or view conceal, invent, or distort a relation central to the claim?
6. Are all plotted features supported by source data, declared assumptions, or explicit construction?
7. Can each geometry-dependent equation/claim be located on the plot, or its abstraction from the plot be explained?
8. Do the equations, symbols, text, and plotted geometry describe the same object?
9. What plausible alternative geometry would invalidate or materially change the claim?
10. What objections remain, and what conclusions are prohibited by the reviewed scope?

The review should be adversarial in method, not ceremonial in tone. It should seek a counterexample, a missing degree of freedom, a topological mismatch, or a representational ambiguity.

## 9. Relationship to existing controls

This proposal strengthens, rather than replaces, the existing controls:

- `FLOORROOM_TODO.md` FF-203 already calls for rigorous code-rendered visuals, Class-P templates, parameter manifests, equation/source pointers, visual QA, and a P/H/I classifier. This proposal makes geometry fidelity and independent review a pre-admission hard gate.
- The existing README correctly warns that CI and Lean results do not establish physical models or H(s)H truth. This proposal further prevents formal results from being admitted without a faithful depiction of the system to which they are claimed to apply.
- The proposed `floor_item.schema.json` is a lifecycle envelope, not yet an operative validator. If this proposal is approved, its geometry fields and state transitions should be added to that schema and to the task graph before implementation.
- H(s)H theory authority remains in HsH BEDROCK and valid Nathan Direct records. This Factory Floor rule governs admission and presentation; it does not itself declare what H(s)H geometry is true.

## 10. Explicit non-effects

Until Nathan explicitly adopts this proposal:
- it is not an operative repository rule;
- it does not modify BEDROCK, theory status, existing item records, or existing Factory Floor stage assignments;
- it does not declare any existing plot accepted or rejected;
- it does not authorize data-free numerical or geometric calculations;
- it does not authorize migration or automated enforcement.

**Decision requested:** Nathan review and explicit adoption, amendment, or rejection.