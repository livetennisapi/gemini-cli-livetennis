# Changelog

All notable changes to this extension are documented here. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.1.0] - 2026-08-07

### Added
- Synced to `livetennisapi-mcp` 1.4.0 — 24 tools (was documented as 12):
  tournaments (`search_tournaments`, `get_tournament`), the 1968–2022 results
  archive (`search_archive_matches`, `get_archive_match`,
  `search_archive_players`, `get_archive_career`), cross-era head-to-head
  (`get_h2h`), ranking tables (`get_rankings`, PRO), per-player rankings as of
  a date (`get_player_rankings`, ULTRA), in-play statistics
  (`get_match_statistics`, ULTRA) and Match Charting Project shot data
  (`get_charting_player`, `get_charting_match`, ULTRA).
- `author` field in `gemini-extension.json`.
- Quota table in the README (grid of 2026-08-06: FREE 100/day, BASIC 1,000/day,
  PRO 10,000/day, ULTRA 500,000/day) with free-key polling guidance.
- `scripts/truthcheck.sh` ground-truth guard, wired into CI.

### Changed
- Server spec floored to `livetennisapi-mcp@^1.4.0` in the manifest.
- Tour phrasing everywhere: ATP, WTA, Challenger, ITF and juniors.
- `GEMINI.md` context rewritten for the full 24-tool surface with per-plan
  gates.

## [1.0.0] - 2026-08-02

### Added
- Initial release: Gemini CLI extension wrapping the Live Tennis API MCP
  server (12 tools), `GEMINI.md` context file, CI manifest validation.
