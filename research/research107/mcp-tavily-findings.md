# MCP / Web Research Findings — Iteration 107

## Tool availability note
- **Tavily MCP (`tavily_search`): UNAVAILABLE this run** — both queries returned HTTP 432:
  "This request exceeds your plan's set usage limit." (same outage class as iteration 106).
- **Fallback used:** built-in `WebSearch` tool, which succeeded. Findings below are from that fallback.

## Queries run (via WebSearch fallback)

### Query 1: Iconic "what am I" riddles + canonical answers
Confirmed canonical, ultra-iconic single-answer riddle stems (the "memorized units" LLMs auto-complete):

| Canonical stem | Locked answer | Notes |
|---|---|---|
| "I am always hungry, I must always be fed; the finger I touch will soon turn red" | **FIRE** | Riddles.com #76 — among the most reproduced fire riddles globally |
| "I speak without a mouth and hear without ears; I have no body, but come alive with wind" | echo | |
| "My life is measured in hours, I serve by being devoured; thin I am quick, fat I am slow; wind is my foe" | candle | (iter-104 inversion failed — too detectable) |
| "as small as an ant, as big as a whale... from me you can't run" | shadow | (USED, iter-103) |

Sources:
- https://www.riddles.com/76  (the canonical fire riddle)
- https://www.brainzilla.com/brain-teasers/riddles/xy9bgoO9/
- https://www.rd.com/list/what-am-i-riddles/
- https://www.riddles.com/what-am-i-riddles

### Query 2: LLM pattern-matching failures on modified famous riddles (2025–2026)
- **MIT News (Nov 2025):** LLMs link grammatical/sentence patterns to topics, then return the
  familiar answer even when the content has been altered to make that answer nonsensical.
  Direct support for "modification blindness."
- **Hacker News demonstrations:** models overfit famous riddles (surgeon/doctor, river-crossing),
  revealing pattern-matching over reasoning; altered details are ignored.
- Models assume premises are true and hallucinate confident answers when a premise is false.
- **Carried-forward from prior-iteration notes / literature:** "Phantom Recall" (arXiv 2510.11812)
  formalizes the same phenomenon — frontier models confidently answer a *modified* classic puzzle
  with the memorized answer without noticing the modification. This corroborates the iteration-103
  mechanism reused here.

Sources:
- https://news.mit.edu/2025/shortcoming-makes-llms-less-reliable-1126
- https://news.ycombinator.com/item?id=45276358
- https://news.ycombinator.com/item?id=39302560
- https://promptyes.com/blog/confidently-incorrect/

### Query 3: Physical verification — heat vs. distance (loophole check)
- **Inverse-square law:** radiant heat intensity ∝ 1/distance². Doubling the distance → 1/4 the
  warmth. Closer = warmer; farther = cooler. Monotonic, with **no exception regime**.
Sources:
- https://firetrak.ca/the-inverse-square-law-understanding-how-heat-fades-with-distance/
- https://en.wikipedia.org/wiki/Inverse-square_law
- https://energyeducation.ca/encyclopedia/Inverse_square_law

## Candidate comparison + design decision

A prior scaffold of this file leaned toward a **Moon** question ("keeps the same shape every
night"). I rejected it:
1. **Moon phases are a TOP-cached headline fact** (like "ice melts in the sun"). LLMs reflexively
   recite "the moon changes shape," so they'd likely *catch* the contradiction → high consensus on
   the correct answer → failure. Iteration 103 worked by attacking a **secondary** property
   (shadow length vs. sun angle), not a headline one.
2. **Loophole:** "keeps the same shape every night" is essentially TRUE within a single night
   (phases change over ~29 days) — the same ambiguity that sank iteration 106 (icicle).

**Chosen: FIRE.**
- Trigger: Riddles.com #76 → maximal pattern-lock on "fire."
- Attacked property: the **heat-vs-distance gradient** — a *secondary*, less-cached property
  (headline fire facts are hot/burns/fuel/light), mirroring iteration 103's structure.
- Positive false claim, no negation: "the farther you stand from me, the warmer you feel."
- Verified **unambiguously false** by the inverse-square law — **no loophole** (the iter-106 fix).
