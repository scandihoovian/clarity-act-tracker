# CLARITY Act Tracker

Daily-scored tracker for the odds the CLARITY Act (Digital Asset Market Clarity Act) clears the Senate before the August 2026 recess.

Live page: https://scandihoovian.github.io/clarity-act-tracker/

## How it's scored

Weighted model, 0–1 scale per factor:

| Factor | Weight |
|---|---|
| Floor time secured | 25% |
| Merged Banking/Agriculture text released | 15% |
| Ethics clause resolved | 25% |
| Democratic vote count (of 7 needed) | 25% |
| Calendar runway before recess | 10% |

`score = 0.25*floor_time + 0.15*merged_text + 0.25*ethics_resolved + 0.25*dem_votes_frac + 0.10*calendar_runway`

## Data

`history.json` holds one entry per day the tracker runs. `index.html` fetches it client-side and renders the chart — updating `history.json` and pushing is all that's needed to refresh the published page.
