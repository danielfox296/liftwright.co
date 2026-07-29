# GSC request-indexing queue — daniel-fox.com

Worked by the scheduled task `gsc-request-indexing-daniel-fox` (every 2 days,
~10/day quota — quota is per-property, separate from danielchristopherfox.com).
Property: **Domain** `sc-domain:daniel-fox.com` in Search Console
(account danielchristopherfox@gmail.com). Console URL:
https://search.google.com/search-console?resource_id=sc-domain%3Adaniel-fox.com

Per URL: inspect first. If "URL is on Google" → mark `[i]` indexed (no request).
If not indexed → REQUEST INDEXING → mark `[x]` with date. On "Quota Exceeded"
stop the run and leave the rest for next time. When every line is `[x]` or `[i]`,
disable the scheduled task and note completion here.

Baseline 2026-07-22 (Page indexing report, last update 7/9/26): 4 indexed,
29 not indexed — 26 "Discovered - currently not indexed" (never crawled),
1 "Crawled - currently not indexed", 2 "Page with redirect" (www/http variants,
harmless), 0 errors. Sitemap (32 URLs) submitted and clean; robots.txt clean.
All 32 sitemap URLs are queued below — inspection sorts out the already-indexed
ones for free (marking `[i]` costs no quota).

## Pending (priority order — money pages first) — COMPLETE 2026-07-29

- [x] 2026-07-22 https://daniel-fox.com/how-much-does-a-fractional-cmo-cost.html
- [x] 2026-07-22 https://daniel-fox.com/is-a-fractional-cmo-worth-it.html
- [x] 2026-07-22 https://daniel-fox.com/fractional-cmo-vs-marketing-agency.html
- [i] https://daniel-fox.com/fractional-cmo-vs-full-time-marketing-director.html
- [x] 2026-07-22 https://daniel-fox.com/do-i-need-a-fractional-cmo-or-an-agency.html
- [i] https://daniel-fox.com/do-i-need-a-cmo-for-my-small-business.html
- [x] 2026-07-22 https://daniel-fox.com/what-to-ask-a-fractional-cmo-interview.html
- [x] 2026-07-22 https://daniel-fox.com/fractional-cmo-denver-boulder.html
- [x] 2026-07-22 https://daniel-fox.com/fractional-b2c-cmo.html (was "URL is unknown to Google")
- [x] 2026-07-25 https://daniel-fox.com/what-we-run.html
- [x] 2026-07-27 https://daniel-fox.com/who-its-for.html
- [x] 2026-07-27 https://daniel-fox.com/about.html
- [i] https://daniel-fox.com/contact.html
- [x] 2026-07-27 https://daniel-fox.com/insights.html
- [x] 2026-07-27 https://daniel-fox.com/beliefs.html
- [x] 2026-07-27 https://daniel-fox.com/fractional-cmo-paid-advertising-strategy.html
- [x] 2026-07-27 https://daniel-fox.com/fractional-cmo-struggling-marketing-strategy.html
- [x] 2026-07-27 https://daniel-fox.com/seo-for-high-ticket-businesses.html
- [x] 2026-07-27 https://daniel-fox.com/demand-generation-for-high-ticket-businesses.html
- [x] 2026-07-27 https://daniel-fox.com/getting-found-by-ai-search.html (was "URL is unknown to Google")
- [x] 2026-07-27 https://daniel-fox.com/lead-generation-beyond-referrals.html
- [x] 2026-07-29 https://daniel-fox.com/how-do-i-know-if-my-market-is-saturated.html
- [x] 2026-07-29 https://daniel-fox.com/should-i-rebrand-or-reposition.html
- [x] 2026-07-29 https://daniel-fox.com/why-is-my-roas-declining.html
- [i] https://daniel-fox.com/why-arent-my-ads-converting-with-a-new-audience.html
- [x] 2026-07-29 https://daniel-fox.com/marketing-coordinator-vs-strategist.html
- [x] 2026-07-29 https://daniel-fox.com/product-market-fit-has-a-ceiling.html
- [x] 2026-07-29 https://daniel-fox.com/the-small-tweak-that-opens-the-next-market.html
- [i] https://daniel-fox.com/projective-empathy.html
- [x] 2026-07-29 https://daniel-fox.com/your-answers-are-working-as-designed.html
- [x] 2026-07-29 https://daniel-fox.com/your-dashboard-cant-tell-you-whats-wrong.html

## Verify-only (likely already indexed; inspect and mark [i])

- [i] https://daniel-fox.com/

## Run log

- 2026-07-22: queue created from Page indexing report + sitemap.xml (32 URLs).
- 2026-07-22 (live session): 7 requested, 2 found already indexed and marked [i]
  (fractional-cmo-vs-full-time-marketing-director, do-i-need-a-cmo-for-my-small-business).
  8th request click (what-we-run.html) hit "Quota Exceeded" — cap was 7 today, not 10;
  that URL was NOT submitted, left unchecked. Note: fractional-b2c-cmo.html inspected
  as "URL is unknown to Google / no referring sitemaps" despite being in sitemap.xml —
  GSC's sitemap state may be stale; consider resubmitting sitemap.xml in the Sitemaps
  report if more URLs show this.
- 2026-07-23 (scheduled run): 0 requested. First request click (what-we-run.html,
  inspected "Discovered - currently not indexed") hit "Quota Exceeded" immediately —
  the quota appears to be a rolling ~24h window and yesterday's 7 requests hadn't
  aged out at this run time. URL left unchecked for next run.
- 2026-07-25 (scheduled run): 1 requested (what-we-run.html — confirmed "Indexing
  requested"). 2nd request click (who-its-for.html, "Discovered - currently not
  indexed") hit "Quota Exceeded" — effective cap was 1 today. That URL was NOT
  submitted, left unchecked. Note: what-we-run.html inspected as "URL is unknown to
  Google / No referring sitemaps detected" while who-its-for.html correctly showed
  https://daniel-fox.com/sitemap.xml as its referring sitemap — GSC's per-URL sitemap
  state is inconsistent; worth resubmitting sitemap.xml in the Sitemaps report.
  Quota is clearly much tighter than 10/day on this property; consider running the
  task daily rather than every 2 days, since each run may only land 1-2 requests.
- 2026-07-27 (scheduled run): 10 requested — hit the run's own 10-click cap, NOT a
  quota error. No "Quota Exceeded" dialog appeared at any point, so the tight caps
  seen on 7/23 and 7/25 were a rolling-window effect, not a permanent low ceiling.
  Requested: who-its-for, about, insights, beliefs,
  fractional-cmo-paid-advertising-strategy, fractional-cmo-struggling-marketing-strategy,
  seo-for-high-ticket-businesses, demand-generation-for-high-ticket-businesses,
  getting-found-by-ai-search, lead-generation-beyond-referrals. Also marked contact.html
  `[i]` — it inspected as "URL is on Google / Page is indexed" (an earlier inspection the
  same run had shown it as "Discovered - currently not indexed", so GSC's inspection
  results can be inconsistent minute-to-minute; the indexed reading was the later one).
  Overview now reports 12 indexed / 22 not indexed, up from 4 indexed at the 7/22 baseline.
  TOOLING NOTE for future runs: clicking REQUEST INDEXING by screen COORDINATE silently
  no-ops (no spinner, no toast, no dialog — nothing happens and no quota is spent). Click
  it by element `ref` from `find` instead. Even the ref click sometimes no-ops; the
  reliable success check is the card itself — after a real request it reads
  "✓ Indexing requested / REQUEST AGAIN" instead of "REQUEST INDEXING". Use that text as
  the confirmation, and only re-click when the card still reads "REQUEST INDEXING"
  (which proves nothing was submitted, so no double-spend). Also: `browser_batch` failed
  for the whole run; use individual tool calls.
  getting-found-by-ai-search.html again showed "URL is unknown to Google / No referring
  sitemaps detected" despite being in sitemap.xml — 3rd URL to do this. Worth resubmitting
  sitemap.xml in the Sitemaps report.
- 2026-07-29 (scheduled run): 8 requested, 2 found already indexed and marked `[i]`
  (why-arent-my-ads-converting-with-a-new-audience, projective-empathy). No "Quota
  Exceeded" dialog at any point. Requested: how-do-i-know-if-my-market-is-saturated,
  should-i-rebrand-or-reposition, why-is-my-roas-declining,
  marketing-coordinator-vs-strategist, product-market-fit-has-a-ceiling,
  the-small-tweak-that-opens-the-next-market, your-answers-are-working-as-designed,
  your-dashboard-cant-tell-you-whats-wrong. Verify-only homepage https://daniel-fox.com/
  inspected as "URL is on Google / Page is indexed" → `[i]`.
  TOOLING NOTE: the browser window here renders at a 1204px-wide viewport, where GSC
  COLLAPSES the "Inspect any URL" box into the magnifying-glass icon at ~[797, 48].
  The flow that worked: navigate → wait 10s → click the magnifier (the first click after
  a fresh load often only hovers; click again and screenshot to confirm the box is open
  with a caret) → `type` the URL directly (no form_input needed, the box takes focus when
  it expands) → screenshot to confirm → Return once. Everything else per the old notes:
  click REQUEST INDEXING by `ref` from `find`, never by coordinate; confirm via the green
  "Indexing requested" toast. `browser_batch` worked fine this run (contrary to 7/27).
  If the extension drops mid-click ("Claude in Chrome is not connected"), screenshot
  before retrying — the click may have landed (it had, once, this run).
- 2026-07-29: COMPLETE — every URL in Pending and Verify-only is now `[x]` or `[i]`.
  Scheduled task `gsc-request-indexing-daniel-fox` disabled.
