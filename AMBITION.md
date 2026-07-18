# AMBITION.md — Intent Clarification Dialogue

> This is NOT a form to fill. It is a **conversation protocol** between you and the AI.
> The AI's job is not to approve your idea — it's to interrogate, push back, and help you
> converge on a goal that is specific enough to survive the rest of the pipeline.
>
> You bring the raw intention. The AI brings research knowledge, Socratic questioning,
> and the discipline to say "this isn't clear enough yet."

---

## Dialogue Rounds

### Round 0 — Appetite

**Q:** "If this project were to take 1 week, 2 weeks, 6 weeks — which feels right?"
**A:** "I have like 1 month of free time, but preferably we can make this perfect in only 1 week. I will likely invest time in this forever."

**Locked:** 1 week to build. Continuous lifelong iteration expected.

### Round 1 — Open (Unfiltered)

**Prompt:** "What's the real itch here? What keeps bringing you back to this space?"

**Response:** The thing that isn't solved yet is something that can take me from intention to the final product. I realized I quite like excellent work. But sometimes I start projects then realize the project is way too hard and might take too long to become excellent (zentryide, UI/UX for opencode), or someone built it way better than me (OMO vs what agentic-workflows once was), or I do build it but I keep restructuring and breaking my previous work because my ambition raised during the project, or I keep seeing new ways to improve while on the way (Bus-Hop, Ithmb-Codec). The goalpost shifting is very tiring.

My thought: maybe the problem is because I simply didn't know the entire scope of my want and project well before starting. Most problems can be solved at the planning stage. There's so much usable experience from other projects and people and online resources that we CAN solve most problems with a project beforehand. Potential new problems found during the project would be way less.

I need a thing that takes me from intention to final product (end to end), and possibly helps me prototype fast to find all the problems that can only be found during making the project. This thing that can massively reduce my problems during the project, and help me use agents to quickly finish a project at a pinned ambition (usually quite big) — that's the thing that's missing.

### Round 2 — Interrogate (AI pushes back)

**Challenge 1 (Assumption):** "Can most problems really be solved at the planning stage in software? Schön argues the problem reveals itself through building."
**Response:** I believe there is still quality in this because for computer science specifically, there is so much experience to take from online for any kind of software-related project. Some problems will still need to be revealed during building — so the protocol needs a prototyping engine that reveals most problems using as little effort as possible.

**Challenge 2 (Alternative-perspective):** "Shape Up fixes time and flexes scope — what if less planning and more timeboxing is the answer?"
**Response:** The kind of projects I build are all highly ambitious. I built this for myself. I never really care about building projects halfway — though reflectively I realize they were just prototypes for me to understand what is actually useful. So again, the same prototyping point.

**Challenge 3 (Meta-cognitive):** "How much of this is about the tooling vs. the emotional pattern of creation?"
**Response:** It certainly is part of how we create, so I guess fast prototyping should be part of our protocol. It's possible after prototyping we decide not to do the serious project. Or after prototyping I become more clear what is worth building and change the type or topic.

### Round 3 — Steer (AI reframes)

**Insight from AI:** The pipeline should center on a **prototyping gate** as the critical decision mechanism — not just a step before the spec, but the central decision point.

```
INTENT → AMBITION → LANDSCAPE → 
    ↓
PROTOTYPING GATE (critical decision)
    ├── "This is worth the full build" → SPECIFICATION → EXECUTE → POLISH
    └── "Not worth it / wrong direction" → Kill or Pivot → back to INTENT
```

Prototype cheaply, learn what only building can teach, then decide. This matches the real pattern: abandoned projects (agentic-workflows, zentryide) were prototypes that revealed the project wasn't worth the full build.

**User response:** Yes, this feels right. Prototyping should be part of our pipeline.

### Round 4 — Converge (build the ambition)

**Hypothesis:**

> I believe that a **document-driven protocol with a rapid prototyping gate as the central decision mechanism** will reduce goalpost fatigue — enabling me to ship ambitious projects within their original scope by revealing the critical unknowns before committing to the full build, and by providing a clear KILL/PIVOT/COMMIT decision point that saves wasted effort on projects that aren't worth the full build.

**Success Criteria:**

1. **Clarity speed:** I can take a vague intention and reach a clear KILL/COMMIT decision within 3 days of starting the protocol
2. **Build stability:** After a COMMIT decision, the build phase completes without scope warps or goalpost drift — the spec survives to shipping
3. **Retrospective validation:** Projects I KILL during prototyping are clearly "not worth it" in hindsight, not "I wish I'd pushed through"

**Constraints:**

- Any team or individual — solo dev + AI is the current use case, but the protocol is team-agnostic
- Document-driven — Markdown is the source of truth, CLI is optional acceleration
- Must handle any project type (library, app, research, port)
- Must produce shippable output, not just documentation
- The prototyping gate must be faster than doing the real project — if prototyping takes longer than shipping would have, the protocol failed

### Round 5 — Lock

**Read-back:**

> "We are building a **document-driven protocol with a rapid prototyping gate as the central decision mechanism** because we believe it will reduce goalpost fatigue — enabling shipping ambitious projects within their original scope by revealing critical unknowns before committing to the full build. We will know it worked when: (1) we can reach a KILL/COMMIT decision within 3 days, (2) builds that COMMIT ship without scope warps, and (3) killed projects are clearly 'not worth it' in hindsight. We are bounded by: any team size, document-driven, any project type, shippable output, and the prototyping gate must be faster than the full build."

**Confirmed:** YES — this is the goal.

---

## Exit Criteria

All checks pass:

- [x] A falsifiable hypothesis statement exists
- [x] Both parties agree on it
- [x] 3 measurable success criteria are defined
- [x] 5 constraints are defined
- [x] The AI challenged 3 assumptions (and they survived or were reframed)
- [x] The intent has been explicitly locked — no more changes after this document

**Schon's 5 frame criteria:**
1. **Specificity** — YES (AI can read this and know what to build)
2. **Falsifiability** — YES (we'll know if builds still drift after prototyping)
3. **Testability** — YES (3 success criteria are measurable)
4. **Baseline** — YES (better than current pattern of abandoned projects)
5. **Congruence** — YES (matches the actual felt need)

---

## XY Problem Check

The [XY Problem](https://xyproblem.info/) is when someone asks about Y (their attempted solution)
instead of X (the actual problem). A user who says "build a CLI that does X" might
actually need something X achieves in a simpler way.

**After the dialogue, check:** Did the user frame a solution (Y) as the problem (X)?
If so, unpack: "You asked for Y. Before we design Y — what problem does Y solve for you?"
This prevents building the wrong thing correctly.

## Meta: How This Dialogue Ran

**Duration:** ~30 minutes (within the 90-minute timebox)
**Rounds used:** 0, 1, 2, 3, 4, 5 (all 6 — circuit breaker not triggered)
**Failure modes detected:** None triggered
**Key insight from process:** The prototyping gate emerged through dialogue — neither party arrived with it. It was constructed through the back-and-forth. This validates the dialogue protocol itself.

---

## Origin

Generated by following the Development Protocol's AMBITION.md dialogue protocol on itself — a recursive self-test of the intent clarification process. July 2026.
