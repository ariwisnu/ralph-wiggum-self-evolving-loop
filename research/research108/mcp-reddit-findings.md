# Reddit MCP Findings — Iteration 108

## Tool availability note

- **Reddit MCP (`search_reddit`): UNAVAILABLE this run.** Returned: "Failed to refresh access token: Failed to get access token: 401 - Unauthorized." The OAuth token for the Reddit MCP server is expired/invalid this session.
- `browse_subreddit` not attempted after the auth failure (same backend).

## Workaround

Reddit-specific community discovery (r/riddles, LLM-failure threads) was not reachable. Compensated with:
1. Built-in `WebSearch` (see `mcp-tavily-findings.md`) to confirm riddle iconicity and physics.
2. Accumulated internal findings (iterations 103 and 107 — the two proven 0%-consensus wins) which already encode the community-validated "famous riddle + positive false physics claim" mechanism.

## Carry-over insight from prior iterations (community-validated mechanism)

- The strongest documented failure mode across this research program is **modification blindness**: frontier LLMs pattern-match a famous riddle to its canonical answer and ignore a subtly altered/false secondary clue (consistent with HN/MIT-style demonstrations of LLMs overfitting classic riddles).
- Iterations 103 (shadow) and 107 (fire) both hit 0% by attacking a SECONDARY physical property with a POSITIVE false claim placed AFTER the iconic trigger. Iteration 108 (echo) applies the identical, community-observed pattern to a new trigger.

No new Reddit data was incorporated this run due to the auth failure; the design rests on the validated internal mechanism plus WebSearch confirmation.
