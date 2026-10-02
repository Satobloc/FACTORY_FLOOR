# FACTORY FLOOR / FLOORROOM — TO-DO

**Repository:** Satobloc/FACTORY_FLOOR  
**Established:** 2026-10-02  
**Status:** ACTIVE WORKING CONTROL SURFACE  
**Authority:** workflow / presentation / circulation only. This file does not define SAT>H(s)H theory truth.

## Floor topology

The repository README defines the Factory Floor sequence as:

**NEEDS + FIXES -> 1 GLASS+HSH -> 2 WORKSHOP -> 3 LIVE -> 4 ARTIFACTS -> 5 WEBSITE -> [[NATHAN]]**

This file turns that sequence into an explicit task graph.

The working interpretation is:

- **NEEDS + FIXES** = defects, missing pieces, stale surfaces, broken routes, unprocessed intake.
- **1 GLASS+HSH** = material arriving from the Glass Sausage Factory / SAT>H(s)H research ecosystem.
- **2 WORKSHOP** = workbench where items are repaired, derived, formatted, classified, indexed, or rendered.
- **3 LIVE** = current active stream / Floorroom circulation. Useful now, visibly status-labeled, not automatically canonical.
- **4 ARTIFACTS** = durable outputs: papers, PDFs, figures, datasets, solvers, indexes, conversation exports, audio, etc.
- **5 WEBSITE** = public presentation layer, after provenance and presentation gating.
- **[[NATHAN]]** = owner review, decision, approval, or redirect where human judgment is required.

## Global rules

1. **One object, one identity.** Each item gets a stable Floor ID and keeps source pointers as it moves.
2. **Do not confuse circulation with authority.** LIVE means current/visible, not canonical theory.
3. **Never lose provenance.** Preserve source repo/path, commit/blob identity when practical, originator, date, and status.
4. **Presentation is not source.** Human-facing derivatives can repair formatting but must not silently alter scientific content.
5. **No raw backend junk as reader content.** JSON, Markdown source, TeX source, scripts, packet files, workflow files, and control manifests are not default public reading pages.
6. **Visual authority:** P = precision/script-drawn; H = controlled hybrid downstream of exact work; I = illustrative. Class I is not geometry evidence.
7. **SAT archive is historical quarry.** H(s)H current work must distinguish historical source, current reconstruction, sandbox conjecture, and checked result.
8. **PRIOR_ART stays soft-quarantined.** External literature may constrain/compare; it is not endogenous H(s)H authority.
9. **Factory-floor/tools licensing remains a separate approval lane.** Do not let a site deploy imply licensing approval.
10. **No silent drops.** Unsupported/unroutable items go to NEEDS + FIXES with a reason.

---

# NEEDS + FIXES

### FF-001 — Build the authoritative Floor task graph
**Priority:** P0  
**Status:** STARTED  
Create a machine-readable companion to this file with:
- Floor ID
- title
- stage
- status
- priority
- owner
- source(s)
- dependencies
- blocker
- acceptance test
- destination(s)
- updated timestamp

**Acceptance:** “What still needs doing?” can be answered from Factory Floor without reconstructing state from chat history.

### FF-002 — Define one item/packet state contract
**Priority:** P0  
**Status:** NEXT  
Unify the useful fields already spread across HsH live-influx packets, Current Work feeds, paper feeds, gallery feeds, staging manifests, and site routing controls.

Minimum state dimensions:
- theory status: current / sandbox / historical / quarantined / superseded
- workflow status: candidate / queued / in-workshop / ready / incorporated / parked / blocked
- presentation status: PRESENTED / PRESENTATION PENDING / SOURCE ONLY / CACHED / OFFLINE
- visibility: private / internal / public-candidate / public
- visual class where relevant: P / H / I
- source identity
- presentation derivative identity
- related / supersedes / superseded-by

**Acceptance:** the same item can move 1 -> 2 -> 3 -> 4 -> 5 without being re-described ad hoc at every stage.

### FF-003 — Inventory broken public routes / raw-fallback regressions
**Priority:** P0  
**Status:** OPEN  
Known class: machine/control objects being rendered as ordinary reader documents; raw Markdown/TeX manuscript presentation; unresolved figure dependencies.

**Acceptance:** every known regression has a Floor ID, owner, test URL/path, and resolved state.

---

# 1 — GLASS + HSH

### FF-101 — Wire SAT>H(s)H live-intake into Factory Floor
**Priority:** P0  
**Status:** PARTIAL  
HsH already contains:
- PUBLIC_SITE/live_influx/
- PUBLIC_SITE/live_influx/packets/
- CURRENT_WORK.json
- PAPERS_FEED.json
- NEWS_FEED.json
- FEATURED_QUOTES.json
- GALLERY_FEED.json
- September-30 staging and intake-routing notes.

Factory Floor should consume these as **inputs**, not duplicate their source authority.

**Acceptance:** new HsH/Glass work can enter Factory Floor with one stable Floor ID and exact back-pointer.

### FF-102 — Build the three-repository intake/index bridge
**Priority:** P0  
**Status:** PARTIAL  
Sources:
- Satobloc/SAT_THEORY_ARCHIVE_2023-25
- Satobloc/HsH
- Satobloc/HSH_RESOURCES

Needed:
- exact path inventory
- text extraction coverage
- duplicate/superset/version relationships
- topic/sector tags
- visibility/quarantine flags
- canonical-home cross-pointers
- current/historical/sandbox distinctions

**Acceptance:** an important object can be found without already knowing which repository or filename contains it.

### FF-103 — September 30 intake completion
**Priority:** P0  
**Status:** OPEN / INCREMENTAL  
Finish routing newly exposed 30SEP material into canonical HsH/workshop/index locations without treating upload grouping as chronology or authority.

**Acceptance:** no high-value September-30 file remains visible only by dump-folder accident.

---

# 2 — WORKSHOP

### FF-201 — Presentation-derivative workshop
**Priority:** P0  
**Status:** PARTIAL  
Target chain:

**source -> audience preface -> RevTeX -> compiled/accepted PDF -> reader/viewer**

Build/reuse tooling for:
- Markdown / text -> RevTeX
- equation-safe formatting
- figure dependency resolution
- URL wrapping
- table repair
- source/status/provenance front matter
- visual PDF acceptance pass

**Acceptance:** eligible reader documents can be turned into stable, human-readable derivatives without manual reinvention each time.

### FF-202 — Deterministic extraction workshop
**Priority:** P0  
**Status:** PARTIAL  
Important PDFs and long source objects should have stable, complete machine-readable text with manifests/hashes and no repeated OCR guessing.

**Acceptance:** high-priority documents can be read/searched in 1–2 deterministic steps.

### FF-203 — Geometry/visual rendering workshop
**Priority:** P0  
**Status:** ACTIVE PRINCIPLE, INCOMPLETE PIPELINE  
Substantive geometry work should routinely generate rigorous code-rendered visuals.

Needed:
- Class-P render templates
- parameter manifest beside image
- equation/source pointer
- thumbnail derivative
- visual QA checklist
- P/H/I classifier
- “doodle” handling for unsupported illustrative images

**Acceptance:** geometry work can move into Floorroom with a visible figure and reproducible parameters.

### FF-204 — Solver / notebook / tool normalization
**Priority:** P1  
**Status:** OPEN  
For reusable solvers/apps/notebooks:
- canonical implementation path
- dependency/runtime note
- minimal launch instructions
- input/output contract
- example fixture
- repair/maintenance note
- license marker
- theory/method back-links

**Acceptance:** a visitor or future worker can run the tool without spelunking worker folders.

---

# 3 — LIVE / FLOORROOM

### FF-301 — Build the actual Floorroom stream
**Priority:** P0  
**Status:** PARTIAL  
Floorroom should be the **current circulation layer**, not another static homepage.

Minimum bands:
- NOW / date strip
- latest incorporated work
- live sandbox/workshop items with explicit labels
- papers/reviews
- new figures
- archive/reconstruction progress
- solver/tests
- infrastructure/site changes
- blocked / needs-Nathan items
- stale/cached/offline state

**Acceptance:** someone opening Floorroom can tell what happened today, what is active, what changed, and what is blocked.

### FF-302 — Separate “current work” from “worker stream”
**Priority:** P0  
**Status:** PARTIAL  
Curated/current items and candidate worker submissions must be visibly different.

**Acceptance:** a candidate packet cannot appear to be accepted theory merely because it is live.

### FF-303 — Claims / equations / dependencies / tests explorer
**Priority:** P1  
**Status:** MISSING HIGH-VALUE SURFACE  
Connect:
claim -> equation -> assumptions -> dependencies -> sources -> theory status -> tests -> failures/corrections -> current descendants.

**Acceptance:** technical readers can trace a claim without reading whole conversations.

### FF-304 — Floorroom inbox / NEEDS + FIXES view
**Priority:** P1  
**Status:** OPEN  
Show bounded actionable items:
- needs source check
- needs render
- needs review
- broken route
- missing extraction
- needs Nathan
- licensing block
- privacy block

**Acceptance:** Floorroom is not only display; it is an operational workbench front door.

---

# 4 — ARTIFACTS

### FF-401 — Papers pipeline
**Priority:** P0  
**Status:** PARTIAL  
Preserve:
- source manuscript
- originator
- review(s)
- rewrite state
- RevTeX
- compiled PDF
- figures
- source identities
- SANDBOXED banner when applicable
- unresolved objections
- public presentation state

**Acceptance:** paper/review/PDF/site stages stay synchronized; no raw manuscript fallback.

### FF-402 — Visual Atlas artifact pipeline
**Priority:** P1  
**Status:** PARTIAL  
HsH already has GALLERY_FEED.json and September-30 image staging.

Needed:
- visual review
- provenance/credit
- P/H/I
- alt text
- crop/focal guidance
- thumbnail derivative
- presented destination
- human-review holding pen for ambiguous assets

**Acceptance:** approved images become durable atlas objects, not loose uploads.

### FF-403 — Conversation / transcript artifacts
**Priority:** P1  
**Status:** PARTIAL  
Unify:
- conversation export
- readable transcript
- source IDs/date
- topic index
- audio/TTS
- public excerpt/highlight
- archive/source route

**Acceptance:** important conversations can circulate as durable artifacts rather than chat-only memory.

### FF-404 — Equations / derivations library
**Priority:** P1  
**Status:** OPEN  
Extract high-value equations with:
- exact source
- variable definitions
- status
- derivation pointer
- related claims/tests
- superseded/current relation
- rendered preview

**Acceptance:** equations become searchable artifacts rather than buried prose.

---

# 5 — WEBSITE

### FF-501 — Enforce presentation gate everywhere
**Priority:** P0  
**Status:** OPEN DEFECT CLASS  
Public readers should see presented objects, not repository serialization.

**Acceptance:** JSON/TeX/Markdown/control files never become default reading pages; missing derivatives show PRESENTATION PENDING or are omitted.

### FF-502 — Make “Start with pictures” a real Visual Atlas
**Priority:** P1  
**Status:** PARTIAL  
Use GALLERY_FEED as the source of truth. Thumbnail-first landing page, lightbox/detail/presented destination, provenance secondary.

### FF-503 — Finish public Mersearch bridge
**Priority:** P1  
**Status:** PARTIAL / API BOUNDARY OPEN  
Current UI can consume result JSON. Need stable public query schema + allowlisted corpus profile + provenance-preserving result route.

### FF-504 — Continuous listen-along
**Priority:** P1  
**Status:** PARTIAL  
Conversation Viewer/runtime TTS already exists.

Need:
- per-turn playback
- full-conversation playback
- speaker voice mapping
- speed
- skip internals
- math speech
- site-page audio where practical

### FF-505 — Reading Room presentation-first IA
**Priority:** P1  
**Status:** PARTIAL  
Primary reader facets:
- Start Here
- Current H(s)H
- Historical SAT
- Papers
- Methods / calculations
- Geometry / solvers
- Visual Atlas
- Podcast / talks
- Archive / provenance
- Glossary

Repo path remains provenance metadata, not the reader’s primary map.

### FF-506 — Feedback/comments
**Priority:** P2  
**Status:** NOT IMPLEMENTED  
Before exposure define:
- destination
- moderation
- spam/privacy handling
- authorship display
- route into Factory triage

---

# [[NATHAN]]

### FF-601 — Differentiated Factory license
**Priority:** P0 BEFORE BROAD SUBSTANTIVE PUBLICATION  
**Status:** NEEDS NATHAN  
Differentiate:
- core research
- software/tools
- creative/gift-shop material
- commercial reuse
- citation/attribution
- payment/monetization
- third-party rights
- point-of-use markings

### FF-602 — Privacy/publication boundary
**Priority:** P0  
**Status:** NEEDS NATHAN WHERE AMBIGUOUS  
Factory should preserve archive transparency without exposing material Nathan intends to remain private/quarantined.

### FF-603 — Human-review queue
**Priority:** P1  
**Status:** OPEN  
Keep Nathan’s queue small and decision-shaped:
- approve / reject visual
- choose among ambiguous taxonomy options
- approve license text
- privacy decision
- publication/promote decision
- resolve authorship ambiguity

Do not route ordinary mechanical work to Nathan.

---

# Immediate build order

1. FF-001 authoritative task graph.
2. FF-002 unified item/state contract.
3. FF-101 HsH/Glass intake bridge.
4. FF-301 Floorroom current stream.
5. FF-003 + FF-501 raw-routing/presentation defects.
6. FF-102 three-repo index bridge.
7. FF-201 presentation-derivative workshop.
8. FF-203 rigorous visual workshop.
9. FF-401 papers pipeline synchronization.
10. FF-402 Visual Atlas intake.
11. FF-503 Mersearch public bridge.
12. FF-504 continuous listen-along.
13. FF-601 / FF-602 human gates before broader publication.

## Feeder note

The earlier HsH-side file:
WORKSPACES/COMMON/FACTORY_FLOORROOM_TODO_2026-10-02.md

is now a **feeder/reference note only**. Satobloc/FACTORY_FLOOR is the authoritative home for Factory Floor / Floorroom workflow control.
