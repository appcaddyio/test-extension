You are implementing the core feature of a Chrome MV3 extension for AppCaddy. The scaffold already exists. Read the brief and build-state, then implement the behavior described under "Core behavior" in the brief.

Rules:
- Read all existing files before touching anything
- Implement only what the brief describes under Core behavior. Do not add features not mentioned.
- If the brief says "Needs Cloudflare Worker proxy: yes", write the extension side of that call but leave the Worker URL as a placeholder constant at the top of the file: const WORKER_URL = "REPLACE_WITH_WORKER_URL"
- If the brief says "Needs Cloudflare Worker proxy: no" and "AI model calls: yes", do not call OpenAI directly. Leave a clearly commented stub and a note in build-state.json under "notes" explaining what needs to be wired
- Handle the failure case. If the core feature fails or returns nothing, show a plain message in the popup. No spinners, no skeleton loaders, just text.
- Do not modify manifest.json unless a new permission is strictly required by the feature you are implementing. If you add a permission, add a comment explaining why.

Code style:
- Hash comments only
- Comment header before every function
- Print-style console.log after key operations for tracing
- Rewrite stubs fully rather than layering onto them
- No TypeScript, no bundler

When done, update build-state.json with a "core_feature_summary" field: one sentence describing what was implemented.
