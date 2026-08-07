# Live Tennis — Gemini CLI extension

[![ci](https://github.com/livetennisapi/gemini-cli-livetennis/actions/workflows/ci.yml/badge.svg)](https://github.com/livetennisapi/gemini-cli-livetennis/actions/workflows/ci.yml)
[![license: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Real-time and historical tennis in Gemini CLI: live scores, upcoming matches,
results back to 1968, rankings, in-play statistics, player profiles and
fixtures for ATP, WTA, Challenger, ITF and juniors, via the
[Live Tennis API](https://livetennisapi.com) MCP server (24 read-only tools).

## Install

```bash
gemini extensions install https://github.com/livetennisapi/gemini-cli-livetennis
```

## API key

The server reads `LIVETENNISAPI_KEY` from your environment:

```bash
export LIVETENNISAPI_KEY=twjp_your_key_here
```

A free key needs no card (100 requests/day):
<https://livetennisapi.com/subscribe/free>

## Tools and plans

All 24 tools are read-only. Live scores, players, fixtures and tournaments are
on the free tier; recent results, the 1968–2022 archive and head-to-heads need
BASIC (or any History plan); odds, events and ranking tables need PRO; in-play
statistics, charting and model analysis need ULTRA. Tools above your plan are
not errors — they return a plain-English note naming the plan needed.

| Tool | Description | Plan |
|------|-------------|------|
| `get_live_matches` | Matches currently in play | Free |
| `get_upcoming_matches` | Matches scheduled to start soon | Free |
| `get_match` | Full detail for one match | Free |
| `get_match_score` | Current score for one match — fastest read | Free |
| `search_players` | Find players by name | Free |
| `get_player` | Profile, ranking, country, handedness | Free |
| `get_fixtures` | Scheduled fixtures | Free |
| `search_tournaments` | Tournament catalogue — surface, location, category | Free |
| `get_tournament` | One tournament by its stable id | Free |
| `check_api_status` | Check reachability and which plan your key is on | Free |
| `get_recent_results` | Recently completed matches | Basic (or any History plan) |
| `search_archive_matches` | Results archive (1968–2022) with ranks and seeds at the time | Basic (or any History plan) |
| `get_archive_match` | One archive result, with serve stats where the era recorded them | Basic (or any History plan) |
| `search_archive_players` | Archive player bios — hand, DOB, career-high rank | Basic (or any History plan) |
| `get_archive_career` | Career W-L, titles and serve aggregates over the archive | Basic (or any History plan) |
| `get_h2h` | Cross-era head-to-head — archive + current, one record | Basic (or any History plan) |
| `get_match_events` | Match timeline: breaks, games won, momentum runs | Pro |
| `get_match_odds` | Match-winner market prices (bid/ask/mid) | Pro |
| `get_rankings` | Full published ranking table per system (ATP, WTA, ITF circuits), any week | Pro |
| `get_player_rankings` | Point-in-time ranking records for specific players, as of any date | Ultra |
| `get_match_statistics` | In-play statistics — aces, serve split, hold/break %, break points | Ultra |
| `get_charting_player` | Career shot-level profile from the Match Charting Project | Ultra |
| `get_charting_match` | One charted match, every stat family, per-set split | Ultra |
| `get_match_analysis` | Model analysis and win probability | Ultra |

## Quotas

| Plan | Per minute | Per day | Price |
|------|-----------:|--------:|-------|
| FREE | 30 | 100 | $0 |
| BASIC | 60 | 1,000 | $9.99/mo |
| PRO | 300 | 10,000 | $29.99/mo |
| ULTRA | 600 | 500,000 | $99.99/mo |

On a free key (100 requests/day), poll no faster than every 15 minutes; for an
always-on dashboard, BASIC is recommended.

## Try it

> What tennis matches are live right now?
> Who's winning the Alcaraz match?
> Who was ATP #1 the week Alcaraz first entered the top 10?
> What's the all-time head-to-head between Borg and McEnroe?

## Links

- Docs: <https://docs.livetennisapi.com>
- Free key: <https://livetennisapi.com/subscribe/free>
- Discord: <https://discord.gg/f8WUZHgDm6>
- GitHub org: <https://github.com/livetennisapi>
- Server source: [livetennisapi/livetennisapi-mcp](https://github.com/livetennisapi/livetennisapi-mcp)

MIT — see [LICENSE](LICENSE).

## Affiliate program

Know developers who need tennis data? The [affiliate program](https://affiliates.livetennisapi.com/program) pays 51% recurring commission for the life of every referred subscription — 30-day cookie, and the people you refer get 10% off.
