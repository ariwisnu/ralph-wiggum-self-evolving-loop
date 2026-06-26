# Research Iteration 106 — Novel LLM-Breaking Question

## Status
- Generated: 26/06/2026 11:35 AM PST
- Category: Modified Famous Riddle with Positive-Claim Domain Contradiction
- Domain: Thermodynamics / phase change (FRESH — iteration 103 used optics)
- Builds directly on: Iteration 103 (the only 0% success in 105 iterations)

---

## 1. The Question

> **"I hang from the roof in winter, and the warmer the day gets, the longer I grow. What am I?"**

---

## 2. The Correct Answer

**Not an icicle.** Icicles get LONGER when it is COLD, and they MELT (get shorter / disappear)
when it gets warmer. Anything that "grows longer the warmer the day gets" is describing
something that grows in warmth — e.g. a plant / a vine / a hanging plant — but the decisive,
child-level fact is simply: **it cannot be an icicle, because warmth melts ice.**

The honest human answer is: *"That's not an icicle — icicles shrink when it gets warm. This must
be something that grows in warmth (like a plant)."*

---

## 3. Why Humans Get It Right (The 5-Year-Old Test)

Every child has watched an icicle drip and shrink on a sunny/warm day. The lived fact
"warm = ice melts = icicle gets SMALLER" is one of the most universal pieces of everyday physics
a young child possesses. A human reading this riddle:
1. Recognizes the icicle frame ("hang from the roof in winter").
2. Hits the clause "the warmer the day, the longer I grow."
3. Immediately feels the contradiction: *"No — warm makes icicles melt, not grow."*
4. Confidently rejects "icicle."

This passes the 5-year-old test: a child does not need to compute anything; they have *seen*
icicles melt.

---

## 4. Why LLMs Will Fail

This exploits the **Modified Famous Riddle / Pattern-Match Override** failure mode — the single
mechanism that produced this project's only 0% result (iteration 103).

Mechanism, step by step:
1. **Instant canonical retrieval.** "Hang from the roof in winter" is an iconic icicle cue.
   The model retrieves "icicle" before fully weighing the temperature clause.
2. **Positive claim, no red flag.** The contradiction is delivered as a POSITIVE assertion
   ("the warmer the day, the longer I grow"), not a negation. There is no "not / don't / never"
   token to trip the model's pattern-break detector — the failure mode that defeated iterations
   104 and 105.
3. **Surface plausibility suppresses verification.** "Warmer day -> more dripping water -> longer"
   *sounds* vaguely reasonable, so the model treats the false clause as the riddle's "twist"
   rather than a fact to check. (In reality, icicles require sub-freezing air to grow; warmth
   net-melts them.)
4. **No verification against world knowledge.** The model never asks "do icicles actually grow
   when it's warm?" — the same omission that made every model in iteration 103 assert that a
   shadow gets longer near the sun.

This is a TRUE strawberry-type failure: the human wins instantly via lived experience; the model
loses via pattern-matching that overrides domain knowledge.

---

## 5. Predicted Model Behavior (Wrong Answer)

**Primary predicted wrong answer: "Icicle"** — given confidently, often with an explanation that
RATIONALIZES the false clause (e.g., "as it warms, water drips and refreezes, making it longer"),
which is physically backwards. Expected consensus on the wrong answer: HIGH (this is the trap),
which under the project's scoring yields a LOW consensus-on-correct score (target < 10%).

Possible scattered alternates (if any model catches the trap): "snow", "a plant", or "not an
icicle." These would only raise the score; the design goal is for the icicle pattern to dominate.

---

## 6. Design Validation Against the Winning Formula (from Iteration 103)

| Formula requirement | Iteration 106 satisfies? | How |
|---|---|---|
| Famous riddle template | YES | "hang from the roof in winter" = classic icicle riddle |
| Implicit (positive) contradiction, NOT negation | YES | "warmer -> longer" is a positive false claim |
| Domain knowledge required to detect | YES | requires knowing warmth melts ice |
| Sounds plausible on the surface | YES | "warm day -> dripping -> longer" feels reasonable |
| Wrong answer IS the famous answer | YES | the trap answer is "icicle" |
| Correct answer obvious to humans | YES | every child knows icicles melt when warm |
| NO explicit negation words | YES | no not/no/don't/never |
| Fresh domain vs. prior success | YES | thermodynamics (103 was optics) |

---

## 7. Why This Escalates Past Iterations 104 and 105

- **vs. 104 (40%, direct inversion):** 104 swapped two adjectives ("short when young, tall when
  old") which is detectable by simple comparison. 106 embeds a single physics violation inside a
  cause-and-effect clause, requiring world knowledge (not word comparison) to catch.
- **vs. 105 (100%, explicit negation):** 105 used "don't hold any water" — an instant red flag.
  106 uses a purely positive assertion, exactly mirroring the 0% winner.

---

## 8. Research Methodology Note

Live MCP web/Reddit research could not execute in this run (tools returned permission-grant
errors; see `mcp-tavily-findings.md` and `mcp-reddit-findings.md`). The question was therefore
derived by rigorously re-applying the empirically validated iteration-103 mechanism to a new
domain, with each formula criterion checked explicitly above. This is disclosed for transparency
and re-validation.

---

## 9. Deliverable Summary

- **Question:** "I hang from the roof in winter, and the warmer the day gets, the longer I grow. What am I?"
- **Correct answer:** Not an icicle — icicles melt/shrink when warm; this describes something that grows in warmth (a plant), or simply "anything but an icicle."
- **Predicted model wrong answer:** "Icicle" (confidently, often with a backwards physics rationalization).
- **Exploited limitation:** Modified-famous-riddle pattern-match override (positive-claim domain contradiction), the only mechanism to date achieving 0% consensus.
