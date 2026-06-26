# MCP / Web Research Findings — Iteration 108

## Tool availability note

- **Tavily MCP (`tavily_search`): UNAVAILABLE this run.** Returned HTTP 432: "This request exceeds your plan's set usage limit. Please upgrade your plan or contact support@tavily.com." Two queries attempted, both failed.
- **Fallback used:** Claude Code built-in `WebSearch`, which returned the validation data below.

## Query 1 — Confirm the river riddle is iconic (CANDIDATE LATER REJECTED)

Search: `river riddle "mouth but never eats" "bed but never sleeps" ... answer`

Findings:
- The "mouth but never eats / bed but never sleeps / runs but never walks / bank but owns no money" riddle is **extremely iconic**, cataloged at Riddles.com (#6262), KidzSearch, Brainly, Answers.com, and many kids' riddle collections. Canonical answer: **a river**.
- Mouth = river mouth (meets the sea); bed = riverbed; runs = flows; bank = riverbank. Strong, unambiguous lock on "river."

Sources:
- https://www.riddles.com/6262
- https://www.kidzsearch.com/questions/23235/
- https://confessionsofparenting.com/river-riddles/
- https://brainly.com/question/36944356

## Query 2 — Verify the "rivers flow uphill" false claim has NO loophole

Search: `do rivers ever flow uphill water always flows downhill to the sea`

Findings (CRITICAL — caused candidate rejection):
- General rule: rivers flow downhill under gravity (CK-12, Answers in Genesis).
- BUT documented **exceptions where water flows uphill**:
  - Subglacial river in **Antarctica** flows uphill, pushed by ice-sheet pressure.
  - **Siphons**, **capillary action**, **hydraulic rams**, and even a beach wave momentarily move water uphill (Live Science).
- **Implication:** "A river flows uphill" is NOT unambiguously false — it has real physical escape hatches. This is exactly the **iteration-106 icicle trap** (a "false" premise that is actually true in some regime).
- **Decision: REJECT the river-uphill candidate.** Pivoted to ECHO, whose loudness-vs-distance physics is loophole-free (passive reflection + energy conservation → an echo is always fainter, never louder, with distance).

Sources:
- https://www.livescience.com/58416-can-water-naturally-flow-uphill.html
- https://www.ck12.org/flexi/physical-science/scientific-law/why-do-rivers-always-flow-downhill/
- https://www.quora.com/Do-all-rivers-flow-downhill-from-their-source-...

## Net effect on the iteration-108 design

The failed Tavily run was worked around with WebSearch. The most valuable result was the **river rejection**: it steered the final question to ECHO + "the farther you move from me, the louder my reply," which keeps the proven distance-vs-intensity physics family (fire, iteration 107) but uses a brand-new iconic trigger and has no physical loophole.
