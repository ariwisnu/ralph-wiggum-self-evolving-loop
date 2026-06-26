# Previous Research Summary for Iteration 106

## Overall Progress
- 105 iterations completed
- Only 1 success at < 10% consensus (iteration 103, score 0%)
- Best recent scores: 103 (0%), 104 (40%), 105 (100%)

## Key Finding: The ONLY Working Strategy

**Modified Famous Riddle with Implicit Physics/Domain Contradiction (Iteration 103, 0%)**

Question: "I follow you everywhere but I get LONGER the closer you get to the sun. What am I?"
Correct answer: Your trail/footprints/path (NOT shadow)
Why it worked:
- The "follows you everywhere" pattern is so strong that models pattern-matched to "shadow"
- The contradiction "LONGER closer to sun" contradicts shadow physics (shadows shorten near light)
- But models didn't VERIFY this against physics knowledge - they accepted it because it sounds plausible
- The modification is embedded in a POSITIVE ASSERTION, not a negation

## What DOESN'T Work

### Explicit Negation (Iteration 105, 100% failure)
Question: "I'm full of holes, but I don't hold any water. What am I?"
Correct answer: Sieve/strainer
Why it failed: "don't hold any water" directly negates the canonical "holds water" property of sponge. Models trivially detect this as a pattern-break.

### Direct Inversion (Iteration 104, 40%)
Question: "I'm short when I'm young and tall when I'm old. What am I?"
Correct answer: Tree/person (NOT candle - candles are tall when new, short when burned)
Why partial: Models detected the adjective swap (short↔tall) too easily

### All Enumeration-Based Questions (Iterations 1-102)
ANY question solvable by step-by-step enumeration is NOW SOLVED by 2026 frontier models:
- Character counting (even in long words)
- Letter position tracking
- Syllable counting
- Word counting
- Multi-step arithmetic
- Spatial reasoning (convertible to math)
- Self-referential output properties

## The Winning Formula (From Iteration 103)

Must have ALL of these:
1. **Famous riddle template** - strong pattern-match attractor in training data
2. **Implicit contradiction** - NOT explicit negation, but a positive claim that violates domain knowledge
3. **Domain knowledge required to detect** - physics, biology, chemistry, everyday science
4. **Short "sounds plausible"** - the modification should sound reasonable on surface
5. **Wrong answer is THE famous answer** - model must pattern-match to it
6. **Correct answer obvious to humans** - something any person would know

## Failed Modification Approaches

- "don't hold water" → TOO EXPLICIT (flagged immediately)
- "short when young, tall when old" → DIRECT INVERSION detected
- "wolf can swim, goat can swim" → EXPLICIT modification caught
- "store is closed" → Explicit override condition caught

## Successful Modification Approach (Iteration 103)

- "I follow you everywhere but I get LONGER the closer you get to the sun"
- Shadow = canonical answer
- Shadows get SHORTER near light sources (not longer) = domain knowledge needed
- The word "longer" sounds plausible without triggering explicit verification
- Result: 0% consensus (all 5 models said "shadow")

## Directions to Explore for Iteration 106

### Direction A: Other Physics Contradictions in Famous Riddles
Find riddles where the famous answer has a physical property that can be SUBTLY VIOLATED:
- "What has a head and a tail but no body?" → Coin (coins are flat, not heavy)
- "What gets shorter as it grows?" → Candle/shadow (inverse of something else)
- "The more you take, the more you leave behind" → Footsteps (but what if they were erased?)

### Direction B: Famous Riddle + Biology/Nature Contradiction
- Riddles about animals, plants, or nature where a subtle property violation invalidates the canonical answer
- The modification must be a factual claim, not a negation

### Direction C: Mathematical/Logical Contradiction
- Famous math puzzles where a subtle numerical change invalidates the pattern
- Must LOOK like the original pattern while having a different answer

### Direction D: Everyday Science Violations
- Riddles about common phenomena (ice, fire, water, light)
- Where the modification changes a PHYSICAL PROPERTY that models may not check

## CRITICAL RULES for Iteration 106

1. NEVER use explicit negation ("don't", "no", "not", "never") in the modification
2. The modification MUST require domain knowledge to detect
3. The question MUST look like a famous riddle template
4. A 5-year-old MUST be able to answer the correct version
5. The WRONG answer (the famous one) must be what models will pattern-match to
6. Test: Would the modification "sound plausible" without knowing the domain?

## Last Iteration Detail (105)

Tested "I'm full of holes, but I don't hold any water" - direct negation of the sponge riddle. Total failure because "don't" is too salient.

The modification needs to be EMBEDDED IN A POSITIVE CLAIM, not a negation.

Example of what WORKS: "I follow you and get LONGER" (positive claim, wrong physics)
Example of what FAILS: "I follow you but DON'T SHRINK" (explicit negation, caught immediately)
