# Smart Upkeep Ideas
Swipe app for improvement ideas for https://webermanapps.github.io/smart-upkeep/. Live: https://webermanapps.github.io/smart-upkeep-ideas/
- `ideas.json` holds the cards (id, title, cat, what, before, after, img). Never change old ids.
- Votes and notes are saved per browser in localStorage key `smartUpkeepIdeasVotes` as `{id:{answer,note,title,time}}` (same pattern as daily-ideas). Share sends a text summary (share sheet, then SMS, then copy).
