# appcaddy-extension-template

Template repo for AppCaddy Chrome extensions. Fork this, fill out brief.md, push to main, and the build pipeline runs automatically.

## How to use

1. Fork this repo and rename it to your tool name
2. Copy brief-template.md to brief.md and fill it out
3. Add ANTHROPIC_API_KEY as a repo secret (Settings > Secrets > Actions)
4. Push brief.md to main
5. GitHub Actions runs the build pipeline across five stages
6. A PR opens when complete. Review it, then merge.

## What gets built

- Complete MV3 Chrome extension scaffold
- Core feature implementation from the brief
- Cloudflare Worker proxy (if brief flags it)
- README and Chrome Web Store copy in AppCaddy voice
- review-summary.md listing what still needs you before shipping

## What you do after merging

- Add icon assets (icons/16.png, icons/48.png, icons/128.png)
- Deploy the Cloudflare Worker and paste the URL into the extension (if applicable)
- Set up the Chrome Web Store listing using store-copy.md
- Create the Polar product if freemium

Published by AppCaddy.
