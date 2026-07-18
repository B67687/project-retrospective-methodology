# Project Context: Development Protocol

## Architecture Decision Log

### ADR-001: Two-Stage Pipeline (2026-07-10)
The protocol now has a two-stage architecture:
1. **PREP PHASE** (pre-protocol) — AMBITION → LANDSCAPE → VALIDATION → SPECIFICATION → EXECUTOR
2. **EXECUTION PHASE** (existing RULES.md) — route-projected phases (WORK/PERFECT/DISTRIBUTE)
3. **POLISH PHASE** — human final pass after execution

Canonical entry point: RULES.md prep-phase block at top of routing tree.

### ADR-002: Docs-First, CLI-Deferred (2026-07-10)
All new protocol documents are standalone Markdown files at repo root (matching existing convention). CLI integration (`pk prep`) deferred to separate work plan.

### ADR-003: Meta-Layer Embedded in Phase Docs (2026-07-10)
Each phase document has an embedded `## Meta` section covering "how to do this well" for that phase. No separate meta-docs.

### ADR-004: Single-Source-of-Truth (2026-07-10)
RULES.md always wins on conflicts between protocol documents. This is documented in the prep-phase entry block.

### Doc Inventory
- `AMBITION.md` — Intent clarification protocol (97 lines)
- `LANDSCAPE.md` — Research protocol (98 lines)
- `VALIDATION.md` — Extended with multi-prototype kill loop, entry-point routing (212 lines)
- `SPECIFICATION.md` — 7-section plan IS spec template + filled example (101 lines)
- `EXECUTOR.md` — Spec-to-RULES.md handoff protocol (109 lines)
- `POLISH.md` — Human final pass, diff from PERFECT/DISTRIBUTE/METHODOLOGY (110 lines)
- `RULES.md` — v2.1.0 with prep-phase entry, SSOT rule, POLISH reference (397 lines)
- `README.md` — Updated with two-stage pipeline diagram and complete Contents table

### Files Not Modified
- `METHODOLOGY.md` — unchanged (POLISH.md references it instead of duplicating)
- `PLAYBOOK.md` — unchanged
- `cli/` — deferred
- `template/` — unchanged
- `docs/` — unchanged
