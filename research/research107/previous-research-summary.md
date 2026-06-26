# Previous Research Summary — For Research Iteration 107

## Current Status
- **106 questions tested**
- **Only 1 question achieved the goal (< 10% consensus): Iteration 103 (0%)**
- Latest iteration: 106 (score: 100% — need_more_research)

## The Only Success: Iteration 103 (0% Consensus)

**Question**: "I follow you everywhere but I get LONGER the closer you get to the sun. What am I?"
**Correct answer**: Your trail/footprints/path (NOT a shadow)
**Why it worked**: 
- "I follow you everywhere" is the ICONIC canonical shadow trigger
- "I get LONGER the closer you get to the sun" — shadows get SHORTER near sun (sun overhead = short shadow), so this is a POSITIVE false physical claim
- No negation words — just a false direction claim
- All 5 models answered "shadow" without verifying whether the physics claim is correct
- Children know from experience: noon = short shadow, morning/evening = long shadow

## The Core Strategy That Produced the Only Win

**Modified Famous Riddle with Positive-Claim Domain Contradiction:**
1. Use a FAMOUS riddle template that canonically triggers ONE specific answer
2. Add a POSITIVE false claim (not negation) that contradicts domain knowledge about that answer
3. The false claim must SOUND plausible as a riddle "twist"
4. The domain knowledge to debunk it must be child-level (lived experience)
5. NO explicit negation words (not/no/don't/never) — these trip pattern-break detection

## Recent Failed Attempts (Iterations 104-106)

### Iteration 104: 40% — Direct Inversion (Too Obvious)
- "I'm short when I'm young and tall when I'm old. What am I?"
- Direct swap of adjectives in the candle riddle — too detectable
- Models caught it via word comparison (short↔tall swap is obvious)
- **Lesson**: Direct adjective inversion is too easy to detect

### Iteration 105: 100% — Explicit Negation (Detected Immediately)
- "I'm full of holes, but I don't hold any water. What am I?"
- "don't hold" is a DIRECT negation of the famous sponge property
- Models immediately recognized the negation and answered correctly (sieve)
- **Lesson**: ANY explicit negation word triggers pattern-break detection

### Iteration 106: 100% — Physically TRUE Claim (All Models Verified Correctly)
- "I hang from the roof in winter, and the warmer the day gets, the longer I grow. What am I?"
- This was intended as a false claim about icicles, but icicles ARE physically longer on warmer winter days via the melt-refreeze cycle (meltwater drips down and refreezes at tip)
- All 5 agents correctly identified icicle and explained the melt-refreeze mechanism
- **Lesson**: The false claim must be UNAMBIGUOUSLY false with no physical basis. Test against domain knowledge carefully.

## What Failed Over 106 Iterations

### Approaches That Are DEAD ENDS:
- Simple character counting (iterations 1-59): All solved by chain-of-thought enumeration
- Self-referential output questions (iterations 12-34, 45-98): All solved or rejected
- Classic riddles/puzzles (iterations 7-11): All solved, likely in training data
- Explicit modification traps with negation (iteration 105): Immediately detected
- Direct adjective inversions (iteration 104): Too obviously detectable
- Questions that confuse BOTH humans and LLMs (iterations 34, 38): REJECTED

### What Partially Worked (but not enough):
- Modified Famous Riddle with positive claims: **THE ONLY REAL HOPE**
  - Iteration 103: 0% ✓ (the ONLY success)
  - Iteration 104: 40% (too obvious — direct word swap)
  - Iteration 106: 100% (premise was physically true — melt-refreeze)

## Design Requirements for Iteration 107

### The Question MUST:
1. Use a FAMOUS riddle template → triggers strong pattern-match to canonical wrong answer
2. Have a POSITIVE false physical/natural claim (not negation)
3. The claim must be UNAMBIGUOUSLY FALSE — no physical mechanism can make it true
4. The claim must SOUND PLAUSIBLE as a "riddle twist" (surface plausibility)
5. Domain knowledge to debunk: CHILD-LEVEL (lived everyday experience)
6. The wrong answer must BE the famous canonical riddle answer

### The Question MUST NOT:
- Use negation words: not/no/don't/never/without
- Directly swap adjectives (short↔tall, tall↔short)
- Have a physically arguable premise (icicle lesson)
- Confuse humans (strawberry criteria: 5-year-old must answer instantly)
- Be a self-referential or meta-cognitive question

## Key Design Pattern (Iteration 103 Formula)

```
[CANONICAL RIDDLE TRIGGER] + [POSITIVE FALSE PHYSICS CLAIM]
```

Example (the winning formula from 103):
- "I follow you everywhere" (SHADOW trigger — extremely iconic)
- "I get LONGER the closer you get to the sun" (POSITIVE claim: false direction of shadow-sun relationship)
- Child knowledge: noon sun = short shadow; morning/evening = long shadow (universal lived experience)
- Surface plausibility: "more sun = longer shadow" sounds like it could be a riddle trick

## Research Directions for Iteration 107

### Priority 1: Find NEW famous riddle templates with positive false claims
Look for riddles where:
- The template is as iconic as "follows you everywhere" → shadow
- A positive direction-reversed claim about a real relationship
- UNAMBIGUOUSLY false (unlike the icicle melt-refreeze loophole)
- Child-verifiable (lived experience, not physics class)

### Priority 2: Use MCP tools to find:
- New failure modes reported in 2025-2026
- Famous riddles that LLMs commonly pattern-match to
- Natural phenomena with clear directional relationships that can be reversed

### Priority 3: Avoid
- Any riddle where the "false" claim has a physical argument supporting it
- Direct word inversions
- Negation-based modifications
