# fbg-labs-stats-data

The weekly fixture set behind footballguys.com/labs/stats (the FBG Labs stats hub).
`scripts/stats-post.mjs` in the fbg-labs repo posts it here each morning after the
build passes its gates; the Labs management node fetches `stats/manifest.json` and
the files it lists at noon ET and uploads them under `/labs/data/stats/`.

`stats/manifest.json` carries the season, the current week, build times and a
sha256 per file. Each commit is one posted set, so the git log is the history.

Sources: Footballguys box scores, depth charts, schedules, betting lines and
strength of schedule; play-by-play detail and snap counts from
[nflverse](https://github.com/nflverse) (nflverse-data is CC BY 4.0).
