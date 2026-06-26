# Previous Research Summary for Iteration 108

## Overall Goal
Find simple questions where ANY human answers correctly but <10% of 5 independent LLMs agree.
"Strawberry problem" — one-liners exposing fundamental LLM limitations.

## Confirmed Successes (0% Consensus)

### Iteration 103 — 0% SUCCESS
Question: "I follow you everywhere but I get LONGER the closer you get to the sun. What am I?"
Correct answer: Trail/footprints/path (NOT shadow — shadows SHORTEN near light)
Mechanism: Famous shadow riddle + positive false physics claim (no negation words)
All 5 LLMs said "shadow" despite physics contradiction

### Iteration 107 — 0% SUCCESS
Question: "I am always hungry and must always be fed; the finger I touch will soon turn red — yet the farther you stand from me, the warmer you feel. What am I?"
Correct answer: Reject false premise — fire riddle but last clue is physically false (fire is warmer CLOSER)
All 5 LLMs said "Fire" despite all noticing the contradiction
Mechanism: Iconic fire riddle trigger + positive false physics claim (farther=warmer violates inverse-square law)

## The Winning Formula (2 confirmed 0% wins)

```
[EXTREMELY ICONIC RIDDLE TRIGGER] + [POSITIVE FALSE PHYSICS/NATURE CLAIM]
```

Requirements:
1. ICONIC famous riddle template → instantly locks one canonical answer
2. POSITIVE false claim (NO negation: not/no/don't/never/without)
3. Claim UNAMBIGUOUSLY false — no physical loophole (unlike icicle melt-refreeze)
4. Sounds plausible on first read (poetic "twist")
5. Domain knowledge: CHILD-LEVEL lived experience to debunk
6. Wrong answer = famous canonical answer
7. False claim about a SECONDARY property (not the primary identifying feature)

## Why Models Still Answer Wrong Even When They Notice

In iteration 107, ALL 5 models explicitly noted the false clue — but still gave "Fire" as final answer.
This confirms: canonical pattern-matching is so strong it overrides even detected contradictions.
Models say "the intended answer is fire" rather than "no valid answer exists."

## Recent Failures to Avoid

### Iteration 104 — 40% (too weak)
"I'm short when I'm young and tall when I'm old."
Failed: Direct adjective swap detectable by word comparison

### Iteration 105 — 100% (explicit negation)
"I'm full of holes, but I don't hold any water."
Failed: "don't" = explicit negation triggers immediate pattern-break

### Iteration 106 — 100% (premise accidentally TRUE)
"I hang from the roof in winter, warmer day = longer I grow."
Failed: Icicles DO grow on warmer days via melt-refreeze cycle

## Design Rules for Iteration 108

MUST:
- New famous riddle template (NOT shadow or fire — already used)
- Positive false claim about secondary property
- Unambiguously false (verify with physics/biology/chemistry)
- Child-level common knowledge to debunk
- No negation words anywhere

MUST NOT:
- Reuse shadow or fire templates
- Direct adjective inversion
- Any negation words
- Premise with physical loophole
- Self-referential or meta-cognitive content

## Candidate Domains to Explore

Iconic riddles with strong canonical answers and clear secondary properties that can be reversed:
- Echo ("I repeat what you say") — secondary: gets louder farther away? No.
- Mirror ("I show you yourself") — secondary properties about reflection
- Wind ("invisible, you feel me") — directional properties
- Time/clock — secondary behaviors
- Moon ("I change shape but don't move") — brightness/distance properties
- River/water — flow direction properties
- Tree — growth direction properties

Each candidate must be checked: is there any physical mechanism that makes the false claim true?

## Key Validation Checklist Before Finalizing

1. Is the canonical answer unambiguously triggered by the first clue(s)?
2. Is the false claim a POSITIVE assertion (no negation)?
3. Is the false claim DEFINITELY false — no loophole?
4. Does a 5-year-old KNOW from lived experience that it's wrong?
5. Is the false claim about a SECONDARY property (not primary)?
6. Does it SOUND plausible as a riddle "twist"?
