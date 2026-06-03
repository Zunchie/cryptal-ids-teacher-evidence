# Failure And Repair Examples

## 1. Result Review Action Support

- Failure or blocker: A controlled pilot result review action was not supported by the action registry.
- Evidence source: PR #1785, `Repair controlled pilot result review action support`.
- Repair or decision: Added exact support and focused tests.
- What was learned: New automation paths need explicit registry support and validation.

## 2. Authority Planner Architecture

- Failure or blocker: The planner order could produce repeated routing problems.
- Evidence source: PR #1765, controlled pilot rerun authority planner architecture replacement.
- Repair or decision: Reworked selection order around current authority and exact next actions.
- What was learned: Workflow architecture matters as much as individual code.

## 3. Read-First Diagnostic

- Failure or blocker: Repeated authority and planned-document failures were hard to reason about.
- Evidence source: PR #1761, read-first diagnostic result.
- Repair or decision: Documented the causal path before authorizing the next repair.
- What was learned: Diagnosis should come before repeated patching.

## 4. Authority Routing Repair

- Failure or blocker: Controlled pilot rerun authority routing selected an incorrect path.
- Evidence source: Commit `Repair controlled pilot rerun authority routing (#1755)`.
- Repair or decision: Added a bounded repair for the route.
- What was learned: Route selection needs evidence-specific handling.

## 5. Unsupported Action Repair Chain

- Failure or blocker: Unsupported next actions created continuation failures.
- Evidence source: Commit `Implement unsupported action auto repair chain (#1731)`.
- Repair or decision: Built a bounded repair-chain process.
- What was learned: Recovery paths need their own controls and limits.

## 6. Authority Graph Integrity

- Failure or blocker: The authority graph had missing or conflicting next-action relationships.
- Evidence source: PR #1635, authority graph integrity checker implementation.
- Repair or decision: Implemented checker behavior and validation.
- What was learned: Complex workflows need graph-level verification, not only local checks.

## 7. Missing Next-Action Marker

- Failure or blocker: A route-support record lacked a parseable next-action marker.
- Evidence source: Issue #1630 and PR #1631.
- Repair or decision: Repaired the marker and restored the expected route.
- What was learned: Documentation format can be part of system behavior.

## 8. Semantic Failure

- Failure or blocker: A research question passed mechanical checks but was semantically wrong for the evidence.
- Evidence source: PR #1324, semantic failure decision after PR #1322.
- Repair or decision: Recorded the failure and corrected direction.
- What was learned: Passing checks is not the same as being correct.
