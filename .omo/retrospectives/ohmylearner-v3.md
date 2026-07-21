# Retrospective: Oh-My-Learner v3 — July 2026

## Applied: Development Protocol v3 (EXTRACTION → REVIEW → ship)

### What Worked

1. **EXTRACTION gate** — Caught the real X ("retention across semesters") behind the stated Y ("flashcard CLI"). This prevented building a tool for the wrong problem.
2. **MECE decomposition** — All 6 dimensions mapped and classified. The "NEEDS PROTOTYPE" flag on AI content quality led directly to the OS card spike, which validated the approach.
3. **Research-interleaved AMBITION** — Tight loop between user input and AI research. The appetite/scope negotiation (3 weeks with trade-offs) was clean.
4. **10 DfC rules** — The size rule caught storage.go (583 LOC) and review.go (269 LOC). Splitting them improved maintainability without breaking anything.
5. **SPEC-first execution** — Writing the spec before implementation in v3 meant zero discrepancy between plan and built (unlike v1→v2 where SPEC-as-built had 19 discrepancies).
6. **Self-explain storage** — Was a "known gap" in v2 SPEC-as-built. v3 closed it.

### What Didn't Work

1. **REVIEW agent routing** — The v3 REVIEW agent (bg_f62e2fcc) spawned but produced no output. Unknown routing issue. Had to manually apply the checklist.
2. **Context management** — This session is extremely long. Multiple compressions were needed. A protocol for "session hygiene" (when to fork to a new session) is missing.
3. **Manual mode blocked compress** — Forced to rely on manual trigger for context management. Reduced efficiency.

### Protocol Updates Needed

- Add "session hygiene" rule: after 100+ tool calls or 3 compressions, fork to a new session with a handoff document
- Fix the REVIEW agent routing (the REVIEW.md says "start a new session" but the tool call didn't produce output)
- Add a MAX_SESSION_LENGTH heuristic (this session is proof that context management is the bottleneck)

### Metrics

| Metric                      | v2         | v3                  |
| --------------------------- | ---------- | ------------------- |
| Tests                       | 38         | 49                  |
| Subject packs               | 2          | 6                   |
| Scheduler                   | SM-2 only  | SM-2 + FSRS-5       |
| Self-explain                | Discarded  | Stored              |
| SPEC-as-built discrepancies | 19 (v1→v2) | 0 (spec-first)      |
| Protocol time               | ~1 month   | 1 session (6 hours) |
