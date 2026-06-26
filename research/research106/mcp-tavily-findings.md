# MCP Tavily Findings - Iteration 106

## Tool Availability Note

In this execution environment, the Tavily MCP tool (`mcp__tavily-web-search__tavily_search`),
the Reddit MCP tools, and the built-in `WebSearch` tool all returned
permission-denied errors ("Claude requested permissions ... but you haven't granted it yet").

Live external web research could NOT be performed in this run. The research below is therefore
synthesized from internal knowledge of (a) the canonical English-language riddle corpus and
(b) the documented LLM failure modes accumulated across iterations 1-105 of this project,
especially the proven success of iteration 103.

This is disclosed transparently so the finding can be re-validated with live search later.

## Synthesized Findings (Internal Knowledge)

### 1. Famous riddles with violable PHYSICAL properties

The strongest pattern-attractor riddles whose canonical answer carries a single, well-known
physical property that can be violated by a POSITIVE CLAIM (no negation):

| Canonical answer | Riddle frame | Violable physical property |
|------------------|--------------|----------------------------|
| Shadow           | "follows you in sunlight" | shortens when sun is HIGH (USED in iter 103) |
| Icicle           | "born in winter, hangs from the roof" | MELTS / shortens when warm |
| Candle           | "gives light, gets shorter" | shortens as it burns (iter 104, too detectable) |
| Echo             | "repeats what you shout"  | grows FAINTER with distance |
| Snowman / snow   | "white, made in winter"   | melts when warm |
| Ice cube         | "cold, clear, in a drink" | melts/shrinks when warm |
| River            | "has a bed, has a mouth"  | flows DOWNHILL |
| Smoke            | "rises from fire"         | rises (less dense than air) |

### 2. Why the THERMODYNAMIC (phase-change) domain is the best fresh target

- Iteration 103 (the only 0% success) used the OPTICS/GEOMETRY domain (shadow length vs. sun angle).
- To ESCALATE and avoid repetition, iteration 106 should use a DIFFERENT domain.
- Phase change (ice melts when warm) is:
  - Universally known, even to a 5-year-old (every child has watched ice melt).
  - Bound to an extremely strong pattern-attractor ("icicle" / "born in winter, hangs from roof").
  - Violable by a clean POSITIVE claim ("the warmer the day, the longer I grow").
  - Superficially plausible (one can imagine warm-day dripping making an icicle "longer"),
    which suppresses model scrutiny while remaining objectively false (warmth net-melts ice;
    icicles GROW only when it is cold enough for dripping water to refreeze).

### 3. Documented LLM failure mechanism reused from iteration 103

- Models lock onto the canonical answer the instant the descriptor matches ("hangs from the roof in winter" = icicle).
- They then ACCEPT the embedded property claim as a riddle "twist" instead of CHECKING it against world knowledge.
- Because the violation is a POSITIVE assertion (not a negation), there is no "not/don't/never"
  red flag to trigger pattern-break detection (the failure mode of iterations 104-105).
