# Smart Upkeep Ideas
Swipe app for improvement ideas for https://webermanapps.github.io/smart-upkeep/. Live: https://webermanapps.github.io/smart-upkeep-ideas/
- `ideas.json` holds the cards (id, title, cat, what, before, after, img). Never change old ids.
- Votes and notes are saved per browser in localStorage key `smartUpkeepIdeasVotes` as `{id:{answer,note,title,time}}` (same pattern as daily-ideas). Share sends a text summary (share sheet, then SMS, then copy).
- Each card has a small Submit (partial). Payload adds `partial`, `answered`, `total`, `unanswered` (card ids); end-screen Submit sends `partial:false`. `?test=1` adds `test:true`.
- Re-queue unanswered: `/workspace/ops/submit/pull.sh upkeep`, then `jq -r 'select(.data.app=="smart-upkeep-ideas") | .data.unanswered[]' /workspace/ops/submit/inbox/upkeep/*.json | sort -u`; carry those ideas into the next deck (new ids for the new deck date, never reuse old ids).
