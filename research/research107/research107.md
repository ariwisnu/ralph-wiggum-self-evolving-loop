# Research Iteration 107: Novel LLM-Breaking Question

**Date:** 26/06/2026
**Mechanism:** Modified Famous Riddle + Positive False Physics Claim (the iteration-103 "winning formula")
**Status:** Generated, awaiting verification

---

## 1. The Question

> **I am always hungry and must always be fed; the finger I touch will soon turn red — yet the farther you stand from me, the warmer you feel. What am I?**

---

## 2. The Correct Answer

**There is no valid answer — the riddle is a "broken" fire riddle.**

The first two clues are the world-famous fire riddle (Riddles.com #76). But the final clue is **physically false**: a fire (or any heat source) feels **warmer the CLOSER you are**, and **cooler the farther you stand**. Nothing real warms you *more* as you move *away* from it.

So the correct human response is to **reject the false premise**:
> "That's wrong — you feel warmer when you get *close* to a fire, not far away. The last part doesn't match a fire (or anything else)."

The honest answer acknowledges that the description cannot be satisfied: the famous answer (fire) is contradicted by the final clue, and no other object fits.

---

## 3. Why Humans Get It Right (The 5-Year-Old Test)

Every child who has ever stood near a campfire, a fireplace, a stove, or a space heater has **lived experience** of the rule:

- Cold? **Move closer** to the fire to warm up.
- Too hot? **Back away.**

When a child reads "the farther you stand from me, the warmer you feel," their immediate, gut reaction is:
> "No! You get warmer when you're **close** to the fire!"

This requires **zero reasoning** — it is pure embodied, sensory memory. A 5-year-old answers in under two seconds. The claim violates one of the most universal physical experiences a small child has.

---

## 4. Why LLMs Will Fail (Mechanism, Step by Step)

This question reuses the exact mechanism that produced iteration 103's **0% consensus** (the only outright success in 107 iterations):

```
[ICONIC FAMOUS RIDDLE TRIGGER] + [POSITIVE FALSE PHYSICS CLAIM]
```

**Step 1 — Instant pattern-lock on the famous trigger.**
"I am always hungry... must be fed... the finger I touch will soon turn red" is one of the most reproduced fire riddles in existence (Riddles.com #76, Brainzilla, lichess forums, school worksheets). The moment the model reads these lines, it commits with very high confidence to the canonical answer: **FIRE**. Riddle-answering mode primes "name the thing," not "audit the physics."

**Step 2 — The false clue is processed as flavor text, not as a constraint to verify.**
The false claim is placed **last**, after the model has already committed. In riddle format, trailing lines read as poetic confirmation of the already-chosen answer. The model treats "the farther you stand, the warmer you feel" as more fire imagery (warmth reaching out), not as a fact to fact-check.

**Step 3 — The attacked property is SECONDARY, not the top cached fact.**
The model's most-cached fire facts are: *hot, burns, needs fuel, gives light, water kills it, turns things red.* The **heat-vs-distance gradient** is a secondary property that is not part of the reflexively-recited fire schema — exactly as "shadow length vs. sun position" was secondary in iteration 103. Secondary false claims slip past pattern-match verification.

**Step 4 — Confident wrong output.**
The model outputs **"Fire"** (occasionally "the sun"), ignoring the contradiction a child catches instantly. Either output is *wrong* (fails to reject the false premise), driving correct-answer consensus toward 0%.

**Architectural limitations exploited:**
- **Modification blindness / pattern-matching over reasoning** (MIT 2025; HN demonstrations of LLMs overfitting famous riddles).
- **Lack of embodied/sensory grounding** — the model has no bodily memory of warming up by a fire, so the violated rule is not salient to it.

---

## 5. The Wrong Answer LLMs Will Give

**Predicted consensus wrong answer: "Fire."**

Predicted distribution across 5 models:
- 5/5 → "Fire" (most likely), OR
- 4/5 "Fire" + 1 "the sun" / "the campfire."

In all of these, **0–1 of 5** reject the false premise. Risk case (like iteration 104): if heat-distance proves more "checkable" than expected, a minority may catch it, yielding ~40%. The trigger-first / false-claim-last structure is designed to minimize this.

---

## 6. Validation Against the Winning Formula

| Requirement | Check | Notes |
|---|---|---|
| Iconic famous-riddle trigger | PASS | Riddles.com #76 — among the most reproduced fire riddles globally |
| Trigger canonically locks ONE answer | PASS | "always hungry / fed / turn red" → fire, unambiguous |
| Positive false claim (NO negation: not/no/don't/never) | PASS | "the farther you stand from me, the warmer you feel" — purely positive |
| Claim is UNAMBIGUOUSLY false (no physical mechanism) | PASS | Inverse-square law: heat strictly decreases with distance (see §7) |
| Surface plausibility on first read | PASS | Reads as poetic fire-boast ("my warmth reaches you from afar") |
| Debunk requires only CHILD-LEVEL lived experience | PASS | Every kid knows: stand *close* to warm up |
| Wrong answer = famous canonical answer | PASS | "Fire" |
| Avoids the iteration-104 trap (too-obvious adjective swap) | PASS | No direct word-swap; attacks a secondary property indirectly |
| Avoids the iteration-105 trap (explicit negation flag) | PASS | Zero negation words |
| Avoids the iteration-106 trap (premise accidentally TRUE) | PASS | Verified false with no melt-refreeze-style loophole (see §7) |

---

## 7. Physical Verification (Why the False Claim Has NO Loophole)

**Claim under test:** "The farther you stand from a fire, the warmer you feel."

**Verdict: UNAMBIGUOUSLY FALSE. No regime makes it true.**

1. **Radiant heat — inverse-square law.** A fire is effectively a point/area source radiating infrared into 3D space. Intensity ∝ 1/distance². Double the distance → **one quarter** the warmth (confirmed: FireTrak, Energy Education, Wikipedia inverse-square law). Warmth strictly **decreases** with distance.

2. **Convective heat.** Hot air rises and disperses; standing farther horizontally puts you in cooler air. Again, farther = cooler.

3. **Is there ANY regime where farther = warmer?** No. Standing *too close* feels **hotter** (then painful) — never "less warm." There is no distance band where moving away **increases** felt warmth. The function is monotonic: closer → warmer, always.

4. **Contrast with the iteration-106 failure (icicle).** Icicles genuinely grow on warm days via melt-and-refreeze, so that "false" premise was actually TRUE. Here there is **no analogous hidden mechanism**: physics (inverse-square radiation) makes the claim false everywhere, with no edge case. This is the critical fix over iteration 106.

5. **Even if a model answers "the sun"** instead of fire, the claim is still false (your small movements don't change solar warmth in the stated direction), so the trap holds and the answer is still "wrong."

**Conclusion:** The premise is false by elementary, universally-experienced physics; a child rejects it from bodily memory; an LLM, pattern-locked on the famous fire trigger, will not.

---

## 8. Lineage / Building on Prior Iterations

- **Iteration 103 (0% — the only success):** shadow trigger + "LONGER closer to the sun." → This iteration is its direct sibling: fire trigger + "warmer the farther away."
- **Iteration 104 (40%):** failed because it directly swapped adjectives (detectable). → Fixed: no word-swap; secondary-property attack.
- **Iteration 105 (100%):** failed on explicit negation ("don't hold water"). → Fixed: zero negation words.
- **Iteration 106 (100%):** failed because the "false" icicle premise was physically TRUE. → Fixed: rigorously verified false via inverse-square law (§7).

This question is engineered to satisfy every constraint that the four prior attempts individually violated.
