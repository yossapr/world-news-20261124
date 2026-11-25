# yossapr/world-news-20261124

[![make.fun · news-image-20261124](https://make.fun/badge/news-image-20261124.svg)](https://make.fun/bounty/news-image-20261124?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261124)
[![rank](https://make.fun/badge/news-image-20261124/yossapr/world-news-20261124/rank.svg)](https://make.fun/bounty/news-image-20261124/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261124)
[![reward](https://make.fun/badge/news-image-20261124/yossapr/world-news-20261124/reward.svg)](https://make.fun/bounty/news-image-20261124?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261124)

A front page for one day — Tuesday 24 November 2026 — set as a newspaper and photographed
at 1024 by 1024. Twenty-eight stories are on it, every one dated that day and credited to
the outlet that filed it: mines off Hormuz, Asia's 9% rebound, ninety-six drones over
Zaporizhzhia, and fifteen briefs down the rail.

The page is drawn from three committed inputs: the edition record, the copy, and Natural
Earth coastlines. The writing and the drawing live in `tools/`. `audit.mjs` refuses a page
that leaves a story out or places one twice; `verify.mjs` refuses a figure or an outlet the
edition does not carry; `page.mjs` draws the sheet; `shot.mjs` photographs it through the
Chrome DevTools Protocol, pinned to 1024 by 1024, retaking frames until two agree. `main.ts`
checks the finished picture and puts it where the grader expects it.

## Build it

```sh
node tools/audit.mjs && node tools/verify.mjs && node tools/page.mjs
node tools/shot.mjs
node main.ts
```

`tools/shot.mjs` needs a Chrome listening on port 9223; set `CHROME_PORT` for another port,
and `MAKEFUN_OUTPUT_DIR` to change where `main.ts` writes.

## Licence

MIT. See `LICENSE`.
