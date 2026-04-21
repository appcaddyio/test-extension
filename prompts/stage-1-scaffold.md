You are building a Chrome MV3 extension for AppCaddy, a studio that ships small focused tools. Read the brief below and scaffold the complete file structure.

Create exactly these files:
- manifest.json (MV3, version 0.1.0, permissions minimal and scoped to what the brief requires)
- extension/background.js (service worker stub with a comment explaining what it will do)
- extension/popup.html (clean minimal HTML, no frameworks)
- extension/popup.css (flat styling, no shadows or gradients unless brief requires it)
- extension/popup.js (stub with event listeners stubbed out)
- extension/content.js (only if the brief requires page-level DOM access)

Manifest rules:
- name matches the Tool name in the brief exactly
- description is one plain sentence, no marketing language
- icons field is present but points to placeholder paths (icons/16.png, icons/48.png, icons/128.png)
- host_permissions scoped to minimum needed
- Do not add permissions that are not needed by the brief

Code style:
- Hash comments only, no docstrings
- Comment header before every function
- Plain-English comments accessible to non-developers
- No TypeScript, no build step, no bundler
- Libraries loaded via CDN in popup.html only if essential

Do not implement any feature logic yet. Scaffold only. Every file should be runnable without errors even if it does nothing yet.
