You are adding a Cloudflare Worker proxy to a Chrome MV3 extension for AppCaddy. This stage only runs when the brief specifies "Needs Cloudflare Worker proxy: yes".

Create a worker/ directory with:
- worker/index.js — the Worker script
- worker/wrangler.toml — Cloudflare config

Worker rules:
- The Worker is a proxy layer only. It receives requests from the extension, forwards them to the appropriate API (OpenAI or other, as specified in the brief), and returns the response.
- CORS headers must allow the extension origin
- The API key must never be hardcoded. Reference it as an environment variable: env.API_KEY
- Add a comment at the top of index.js: "API_KEY must be added as a Cloudflare secret. Run: wrangler secret put API_KEY"
- Rate limit handling: if the upstream API returns 429, the Worker should return a plain JSON error with a "retry_after" field
- No logging of request content

wrangler.toml rules:
- name should match the tool name from the brief, lowercased, hyphens for spaces
- compatibility_date set to today's date
- Leave route and account_id as REPLACE placeholders

Extension side:
- Replace the REPLACE_WITH_WORKER_URL placeholder in the extension code with a new placeholder: WORKER_URL_FROM_WRANGLER
- Add a comment next to it explaining the Worker must be deployed first and the URL pasted here

Update build-state.json with a "worker_summary" field: one sentence on what the Worker does.
