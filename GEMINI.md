# Live Tennis extension

This extension gives you 24 read-only tennis tools backed by the Live Tennis
API: live scores, upcoming matches, recent results, full match detail, current
score, match events, in-play statistics, player search and profiles, fixtures,
tournaments, ranking tables, per-player rankings as of a date, a 1968–2022
results archive with player bios and career aggregates, cross-era
head-to-heads, Match Charting Project shot data, match-winner market prices,
model analysis, and an API status check. Coverage: ATP, WTA, Challenger, ITF
and juniors.

Useful conventions:

- Prefer `get_live_matches` for "what's on right now" and `get_match_score`
  for the fastest score-only read of a known match.
- Tennis scores read player-major: `games` is `[[p1 per set], [p2 per set]]`,
  `points` are strings ("40", "AD"), and `server` may be null for a moment
  between games.
- History questions split cleanly: `search_archive_matches` (1968–2022)
  answers "Borg's Wimbledon finals", `get_recent_results` answers "yesterday's
  scores", and `get_h2h` spans both eras in one record.
- Rankings come in two shapes: `get_rankings` lists a full published ranking
  table (ATP, WTA, ITF circuits) for any week; `get_player_rankings` answers
  "what was this player ranked on that date".
- Tools behind a paid plan return a plain-English note naming the plan rather
  than an error — relay it as-is. Per tool: `get_recent_results`,
  `search_archive_matches`, `get_archive_match`, `search_archive_players`,
  `get_archive_career` and `get_h2h` need BASIC (or any History plan);
  `get_match_events`, `get_match_odds` and `get_rankings` need PRO;
  `get_player_rankings`, `get_match_statistics`, `get_charting_player`,
  `get_charting_match` and `get_match_analysis` need ULTRA. Everything else
  (live/upcoming matches, single-match detail and score, players, fixtures,
  tournaments, status check) works on the free tier.
