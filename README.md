# kaila-job-search

Weekly job board for Kaila. Served by Cloudflare Workers static assets at https://kaila-job-search.rob0labs.workers.dev

- `public/index.html` is the board. It is written once and never rewritten by weekly runs.
- Weekly runs add `data/scans/YYYY-MM-DD.json` and append the file name to `data/manifest.json`.
- The deploy workflow copies `data/` into `public/data/` before `wrangler deploy`.
