# Development Protocol — Self-RULES.md

**Project:** Development Protocol v3
**Phase:** DISTRIBUTE (stable, ready for external use)
**Project type:** STANDARD (document-driven, familiar domain, clear spec)
**Location:** /home/nami/projects/dev/Development-Protocol/
**Updated:** 2026-07-21

## 1. Project Type Routing

| Route          | Status | Reason                             |
| -------------- | ------ | ---------------------------------- |
| DISCOVER-FIRST | N/A    | Domain is well-understood          |
| STANDARD       | ✅     | Documentation project, clear scope |
| MAINTENANCE    | N/A    | Not a deployed system              |

## 2. Intent Decomposition

The protocol has been decomposed into 15 documents across 3 gates:

- **Gate 0:** EXTRACTION.md + FUNDAMENTALS.md (problem discovery)
- **Gate 1:** AMBITION.md (appetite and scope)
- **Gate 2:** VALIDATION.md (prototype decision)
- **Execution:** SPECIFICATION.md → EXECUTOR.md → POLISH.md → EXPLAINER.md → SPEC_SYNC.md → REVIEW.md
- **Governance:** RULES.md (this file), shift-log.md

## 3. Constitution

1. **Provenness requirement** — Every technique in the protocol must have an empirical citation or pass its own validation before entering.
2. **Recursion meta-rule** — Every step is recursive. If output is still ambiguous after one pass, apply the step again.
3. **Clarify the language** — Before any extraction, assume you don't know what the user means. Restate in different words and confirm.
4. **Independence in review** — The REVIEW agent must be a separate session with no prior context.
5. **Design for change** — Goalpost shifts are learning, not failures. Up to 5 documented shifts per project.
6. **Defaults before custom** — Standard choices validated by 10,000 projects need zero additional validation.

## 4. Phase Definitions

| Phase      | Status         | Key Deliverable                          |
| ---------- | -------------- | ---------------------------------------- |
| DISCOVER   | ✅ Complete    | X extraction, fundamentals analysis      |
| WORK       | ✅ Complete    | All 15 documents written                 |
| PERFECT    | ✅ Complete    | Integration, cross-references, debugging |
| DISTRIBUTE | ✅ **Current** | Final review, README, release            |

## 5. Learning Shifts

| #   | What we learned                                         | Decision                                             | When       |
| --- | ------------------------------------------------------- | ---------------------------------------------------- | ---------- |
| 1   | XY Problem needs an explicit step before decomposition  | Created EXTRACTION.md                                | 2026-07-19 |
| 2   | Language ambiguity is more fundamental than XY problems | Added "Clarify the Language" to EXTRACTION.md        | 2026-07-20 |
| 3   | Goalpost shifts are evidence of learning, not failure   | Changed "Scope Warps" to "Learning Shifts" (max 3→5) | 2026-07-19 |
| 4   | Standard validation depth depends on risk, not dogma    | Added FUNDAMENTALS.md with depth decision tree       | 2026-07-21 |
| 5   | Recursion is a meta-pattern across all protocol steps   | Added recursion meta-rule to RULES.md                | 2026-07-21 |

## 6. AI Persona & Constraints

- **Persona:** Requirements engineer + methodology designer
- **Autonomy:** HIGH for content improvements, LOW for structural changes (must confirm)
- **Prohibited:** Removing gates, bypassing independence, adding features without citations

## 7. Stop Rules

- New document in the pipeline → plan first
- Changing the Constitution → must run REVIEW on the change
- Removing a gate → confirm with user
- Adding a technique without a citation → refuse (provenness requirement)

## 8. Verification Gates

| Gate                     | When                                               | What checks                       |
| ------------------------ | -------------------------------------------------- | --------------------------------- |
| EXTRACTION completion    | X must be one sentence, no solution words          | 3+ techniques converged           |
| FUNDAMENTALS completion  | One-way doors identified and validated or deferred | Minimum prototype for each        |
| AMBITION completion      | Appetite set, scope bounded                        | Both parties confident            |
| SPECIFICATION completion | All 14 sections filled                             | No "TBD" or blank sections        |
| REVIEW                   | Before DISTRIBUTE                                  | 24-item checklist, 3 gates passed |

## 9. Test Philosophy

The Dev Protocol is a documentation project. "Tests" are:

- Internal consistency checks (cross-references between documents)
- Self-application (the protocol can successfully guide its own improvement)
- Meta-review (REVIEW.md run on itself)

## 10. Evolution & Phase Exit

DISTRIBUTE exit criteria:

- [ ] All 15 documents exist and are internally consistent
- [ ] Pipeline diagram shows correct flow
- [ ] REVIEW completed with no MAJOR/CRITICAL findings
- [ ] Learning shifts documented (5 shifts recorded)
- [ ] Handoff document exists for external users

## 11. Known Failure Patterns

| FP     | Name                      | Mitigation                                               |
| ------ | ------------------------- | -------------------------------------------------------- |
| FP-001 | Cherry-picking techniques | Must apply 3+ techniques in EXTRACTION                   |
| FP-002 | Over-validation           | FUNDAMENTALS.md says: standard choices = zero validation |
| FP-003 | False independence        | REVIEW.md independence protocol                          |
| FP-004 | Scope creep               | Appetite before scope                                    |

## 12. Session Kickoff

First session tasks:

1. Read this RULES.md
2. Read the current REVIEW findings
3. Determine if DISTRIBUTE exit criteria are met
4. If yes: tag release and update README
5. If no: fix remaining items
