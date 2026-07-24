# Live Tennis extension

This extension gives you twelve read-only tennis tools backed by the Live
Tennis API: live scores, upcoming matches, recent results, full match detail,
current score, match events, player search and profiles, fixtures, match-winner
market prices, model analysis, and an API status check.

Useful conventions:

- Prefer `get_live_matches` for "what's on right now" and `get_match_score`
  for the fastest score-only read of a known match.
- Tennis scores read player-major: `games` is `[[p1 per set], [p2 per set]]`,
  `points` are strings ("40", "AD"), and `server` may be null for a moment
  between games.
- Tools behind a paid plan (odds, analysis) return a plain-English note naming
  the plan rather than an error — relay it as-is.
