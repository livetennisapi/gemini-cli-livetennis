# Live Tennis — Gemini CLI extension

Real-time tennis in Gemini CLI: live scores, upcoming matches, results, player
profiles and fixtures for ATP, WTA, Challenger and ITF, via the
[Live Tennis API](https://livetennisapi.com) MCP server (12 read-only tools).

## Install

```bash
gemini extensions install https://github.com/livetennisapi/gemini-cli-livetennis
```

## API key

The server reads `LIVETENNISAPI_KEY` from your environment:

```bash
export LIVETENNISAPI_KEY=twjp_your_key_here
```

A free key needs no card (1,000 requests/day):
<https://livetennisapi.com/subscribe/free>

## Tools and plans

All 12 tools are read-only. Live scores, players and fixtures are on the free
tier; recent-results listings need BASIC or any History plan; odds and model
analysis need PRO/ULTRA. Tools above your plan are not errors — they return a
plain-English note naming the plan needed.

| Tool | Description | Plan |
|------|-------------|------|
| `get_live_matches` | Matches currently in play | Free |
| `get_upcoming_matches` | Matches scheduled to start soon | Free |
| `get_match` | Full detail for one match | Free |
| `get_match_score` | Current score for one match | Free |
| `search_players` | Find players by name | Free |
| `get_player` | Profile and ranking for one player | Free |
| `get_fixtures` | Scheduled fixtures | Free |
| `check_api_status` | Check reachability and which plan your key is on | Free |
| `get_recent_results` | Recently completed matches | Basic (or any History plan) |
| `get_match_events` | Match timeline: breaks, games won, momentum runs | Pro |
| `get_match_odds` | Match-winner market prices (bid/ask/mid) | Pro |
| `get_match_analysis` | Model analysis and win probability | Ultra |

## Try it

> What tennis matches are live right now?
> Who's winning the Alcaraz match?
> Show me Sinner's ranking and recent results.

Server source: [livetennisapi/livetennisapi-mcp](https://github.com/livetennisapi/livetennisapi-mcp) · MIT
