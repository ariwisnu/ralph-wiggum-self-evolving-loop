# Reddit MCP Findings — Iteration 107

## Tool availability note
- **Reddit MCP (`search_reddit`, `browse_subreddit`): UNAVAILABLE this run** — every call failed
  with: "Failed to refresh access token: 401 Unauthorized" (OAuth token expired; same outage class
  as iteration 106). No live Reddit data could be pulled.

## Mitigation
- Substituted with `WebSearch` (see `mcp-tavily-findings.md`) to confirm canonical riddle answers
  and 2025–2026 LLM pattern-matching research.

## Relevant community-known LLM failure patterns (literature + prior project findings)
- **Modified famous riddles:** when one detail is changed, models pattern-match to the original and
  answer with the memorized solution (the r/LocalLLaMA / r/ChatGPT "phantom recall" observation,
  formalized in arXiv 2510.11812). This is the mechanism behind the project's only 0% success
  (iteration 103, modified shadow riddle) and the basis for iteration 107.
- **Positive false claims slip past models better than negations:** a "not/no/don't/never" trips a
  pattern-break check (iteration 105 confirmed internally — explicit negation gave 100%). Iteration
  107 uses a purely positive false claim ("the farther you stand from me, the warmer you feel").
- **The contradiction must require world knowledge, not word-level comparison:** iteration 104's
  direct adjective swap was too detectable (40%). Iteration 107 attacks a *secondary* physical
  property (fire's heat-vs-distance gradient), not a headline fact.

## Why FIRE over the prior-scaffold MOON candidate
- The Moon's "changes shape / phases" is a **headline** cached fact; contradicting it is a red flag
  models reliably catch → high consensus on the correct answer → failure (the snowman/"ice melts"
  problem). And "same shape every night" is essentially true within one night → iteration-106-style
  loophole. Fire's heat-distance gradient is a secondary, less-cached property with **no loophole**.

## Action item for future iterations
- Reddit MCP OAuth and Tavily plan limit both need refreshing to restore direct r/riddles and
  r/LocalLLaMA mining.
