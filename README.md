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

Scores, players and fixtures are on the free tier; odds and model
win-probability tools require the PRO and ULTRA plans and explain as much when
called on a free key.

## Try it

> What tennis matches are live right now?
> Who's winning the Alcaraz match?
> Show me Sinner's ranking and recent results.

Server source: [livetennisapi/livetennisapi-mcp](https://github.com/livetennisapi/livetennisapi-mcp) · MIT
